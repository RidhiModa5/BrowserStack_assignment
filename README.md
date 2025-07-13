# BrowserStack_assignment

A comprehensive web scraping solution that automates news article extraction from El País (Spanish news outlet), translates content, analyzes text patterns and returns the words having frequency greater than 2, and runs cross-browser tests on BrowserStack.

## 🚀 Features

- **Web Scraping**: Automated extraction of articles from El País Opinion section
- **Content Processing**: Downloads article images and extracts text content
- **Translation**: Spanish to English translation using Google Translate API
- **Text Analysis**: Word frequency analysis across translated headers
- **Cross-Browser Testing**: Parallel execution across 5 different browser configurations on BrowserStack
- **Comprehensive Logging**: Detailed execution logs and error handling
- **Data Export**: Results exported to Excel format with organized file structure

## 📋 Requirements

### Python Dependencies
```
selenium==4.15.2
requests==2.31.0
googletrans==4.0.0rc1
pandas>=1.5.0
openpyxl>=3.0.0
python-dotenv>=1.0.0
browserstack-local==1.2.12
```

### External Services
- **BrowserStack Account**: Free trial account for cross-browser testing
- **Google Translate API**: For text translation (uses free googletrans library)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the project root directory:
   ```env
   BROWSERSTACK_USERNAME=your_browserstack_username
   BROWSERSTACK_ACCESS_KEY=your_browserstack_access_key
   ```

4. **Create BrowserStack account**
   - Visit [BrowserStack](https://www.browserstack.com/)
   - Sign up for a free trial account
   - Get your username and access key from Account Settings

## 🚀 Usage

### Basic Execution
```bash
python main.py <absolute_directory_path_to_store_results>
```

### Example
```bash
python main.py /home/user/browserstack_results
```

## 📁 Output Structure

After successful execution, the specified directory will contain:

```
results_directory/
├── browserstack_screenshots/         # Full page screenshots
│   ├── opinion_page_chrome.png
│   ├── opinion_page_firefox.png
│   └── ...
├── article_images/               # Downloaded article cover images
│   ├── article_1_cover.jpg
│   ├── article_2_cover.jpg
│   └── ...
├── ElPais_Analysis_YYYYMMDD_HHMMSS.xlsx  # Comprehensive analysis report
├── execution_YYYYMMDD_HHMMSS.log                # Detailed execution logs
```

## 📊 Excel Report Contents

The generated Excel file contains multiple sheets:

- **Article_Details**: Complete article information (titles, content, URLs)
- **Translated_Headers**: Original Spanish titles and English translations
- **Word_Frequency**: Analysis of repeated words across all headers
- **Browser_Results**: Cross-browser execution results and performance metrics
- **Execution_Summary**: Overall statistics and success rates



```
project/
├── main.py                 # Main execution script
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables
└── README.md             # This file
```

## 🚀 Performance Optimization

### Current Optimizations
- Parallel execution across 5 browser instances
- Efficient image downloading with proper error handling
- Cached translation results to avoid duplicate API calls
- Optimized element waiting strategies

