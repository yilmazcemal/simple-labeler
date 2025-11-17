# Mobile Classifier App

A lightweight, mobile-optimized HTML application for binary classification of CSV data. Perfect for data labeling, annotation tasks, and manual classification workflows on any device.

## Features

- **📱 Mobile-First Design**: Optimized for touch interfaces with swipe navigation
- **📊 Universal CSV Support**: Works with any CSV file structure
- **🎯 Flexible Column Selection**: Choose which column to classify from your dataset
- **⚡ Quick Navigation**:
  - Swipe left/right to navigate between rows
  - Arrow buttons for precise control
  - Jump directly to any row by number
- **📈 Progress Tracking**: Visual progress bar showing classification completion
- **👁️ Data Preview**: View all your data and classifications in a table
- **💾 Export Results**: Download labeled data with timestamp
- **🔄 Auto-Advance**: Automatically jumps to next unlabeled item after classification
- **🌐 Offline Capable**: No internet connection required - runs entirely in browser

## Usage

### Getting Started

1. **Open the App**: Simply open `villain_classifier_mobile.html` in any modern web browser
2. **Load Your CSV**: Click the file input and select your CSV file
3. **Select Column**: Choose which column you want to classify from the dropdown
4. **Start Classifying**: Click "Start Classification" to begin

### Navigation

- **Swipe Left**: Go to next row
- **Swipe Right**: Go to previous row
- **Arrow Buttons**: Navigate one row at a time
- **Row Number Input**: Type a row number and press Enter to jump directly

### Classification

- **✅ Not Villain Button** (Green): Mark current item as class 0
- **🦹 Villain Button** (Red): Mark current item as class 1

The app automatically advances to the next unlabeled item after classification.

### Viewing & Exporting

- **📊 View Data**: Opens a modal showing all rows and their classification status
- **💾 Export**: Downloads CSV file with format: `[original_filename]_labeled_YYYY-MM-DD_HHMM.csv`

## File Format

### Input CSV Requirements

- Standard CSV format with headers
- UTF-8 encoding supported
- Can contain any number of columns
- Quoted fields and commas within fields are properly handled

### Output Format

The app adds a `villain` column to your CSV with values:
- `1` = Villain (positive class)
- `0` = Not Villain (negative class)
- Empty = Not yet labeled

### Example

**Input CSV:**
```csv
id,sentence,author
1,"This is a sample text",John
2,"Another example",Jane
```

**Output CSV:**
```csv
id,sentence,author,villain
1,"This is a sample text",John,1
2,"Another example",Jane,0
```

## Technical Details

- **Pure HTML/CSS/JavaScript**: No dependencies or frameworks required
- **Browser Compatibility**: Works on modern browsers (Chrome, Firefox, Safari, Edge)
- **Mobile Support**: Tested on iOS and Android devices
- **Touch Optimized**: Custom swipe gesture handling for smooth mobile experience
- **UTF-8 Support**: Handles international characters correctly with BOM handling

## Customization

You can easily customize the classification labels by modifying the button text and class names in the HTML:

- Line 322-327: Button labels and styling
- Line 555-578: Auto-advance and labeling logic
- Line 534-543: Label display text

## Use Cases

- Text classification and sentiment analysis
- Image/document annotation
- Quality assurance checks
- Survey response categorization
- Content moderation
- Training data preparation for ML models
- Manual review workflows

## Tips

- **Keyboard Shortcuts**: On desktop, you can tab through controls for faster classification
- **Progress Tracking**: The progress bar shows percentage of labeled items, not current position
- **Data Safety**: Your data never leaves your device - everything runs locally
- **Resume Later**: Close and reopen the app with the same CSV to continue where you left off
- **Batch Processing**: Export regularly to save your progress

## License

This project is open source and available for use in your own projects.

## Contributing

Suggestions and improvements are welcome! This is a standalone HTML file, so modifications are straightforward.

---

**Built with Claude Code for efficient mobile data classification workflows** 🚀
