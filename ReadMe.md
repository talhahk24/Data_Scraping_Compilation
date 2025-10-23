# Data Scraping Compilation

This repository contains comprehensive data scraping solutions for various organizations and websites. The projects demonstrate advanced web scraping techniques using Selenium WebDriver, data processing with pandas, and automated data extraction workflows.

## Project Files

### 1. Food Data Scraping (Center for Food and Safety)
**File:** `Food_Data_Scraping_(Center_for_Food_and_Safety).ipynb`

**Description:** A modular, multi-language food nutrition data scraper for the Hong Kong Center for Food and Safety website.

**Features:**
- **Multi-language Support**: English, Traditional Chinese, and Simplified Chinese
- **Modular Architecture**: Clean, reusable `FoodDataScraper` class
- **Comprehensive Data**: Food categories, nutritional information, and food IDs
- **Automated Workflow**: Complete scraping pipeline with error handling
- **CSV Export**: Structured data output for analysis
- **Screenshots**: Automatic documentation of scraping process

**Data Sources:**
- English: `https://www.cfs.gov.hk/english/nutrient/search1.php`
- Traditional Chinese: `https://www.cfs.gov.hk/tc_chi/nutrient/search1.php`
- Simplified Chinese: `https://www.cfs.gov.hk/sc_chi/nutrient/search1.php`

**Output Files:**
- `Eng_With_ID_All_Categories_Data.csv`
- `TC_With_ID_All_Categories_Data.csv`
- `SC_With_ID_All_Categories_Data.csv`

**Key Technologies:**
- Selenium WebDriver with Chrome headless mode
- Pandas for data manipulation
- Google Cloud Translation API integration
- Modular class-based architecture

---

### 2. Rotary Club, Travel Industry, & Home Affairs Department Data Scraping
**File:** `(November_2023)_DataScraping_Tasks_Socif_Limited.ipynb`

**Description:** Professional data extraction solutions for Rotary Club directories and Travel Industry Council of Hong Kong agent listings.

**Features:**
- **Rotary Club Directory**: Complete club information extraction
- **Travel Agent Database**: Comprehensive agent contact details
- **Multi-page Scraping**: Automated pagination handling
- **Window Management**: Advanced tab switching and navigation
- **CSV Export**: Structured contact databases
- **Performance Optimization**: Reduced wait times and efficient scrolling

**Data Sources:**
- Rotary Club Search: `https://my.rotary.org/en/club-search`
- Travel Industry Council: `https://tichk.org/zh-hant/agents/find-agent`
- Home Affairs Department: `https://bmis2.buildingmgt.gov.hk/bd_hadbiex/content/searchbuilding/building_search.jsf`

**Output Files:**
- `club_data.csv` - Rotary Club information
- `agent_data.csv` - Travel agent contact details
- `buildings_data.csv` - Building management data

**Extracted Data Fields:**
- **Rotary Clubs**: Name, Email, Phone, Language
- **Travel Agents**: Name, Phone, Email
- **Building Management**: Name, Organisation, Incorporated Owner

**Key Technologies:**
- Selenium WebDriver with custom scrolling functions
- Dynamic page loading and element detection
- CSV data export with UTF-8 encoding
- Error handling and timeout management

#### **3. Home Affairs Department Building Data**
**Part of:** `(November_2023)_DataScraping_Tasks_Socif_Limited.ipynb`

**Description:** Large-scale building management data extraction from Hong Kong's Home Affairs Department building information system.

**Features:**
- **Building Database**: Comprehensive building information extraction
- **Massive Scale**: 42,000+ building records across multiple checkpoints
- **Advanced Pagination**: Automated navigation through thousands of pages
- **Progress Tracking**: Checkpoint-based data collection with progress monitoring
- **Google Drive Integration**: Direct CSV export to Google Drive
- **Screenshot Documentation**: Visual progress tracking and debugging

**Data Source:**
- Home Affairs Building Management: `https://bmis2.buildingmgt.gov.hk/bd_hadbiex/content/searchbuilding/building_search.jsf`

**Output Files:**
- `buildings_data.csv` - Complete building management database

**Extracted Data Fields:**
- **Building Name**: Official building names
- **Organisation**: Managing organizations
- **Incorporated Owner**: Property ownership information

**Technical Features:**
- **Checkpoint System**: Data collection in 3,000-record batches
- **Language Switching**: Multi-language interface support
- **Pagination Optimization**: 20 entries per page for efficiency
- **Error Recovery**: Robust handling of page loading issues
- **Progress Monitoring**: Real-time progress tracking and status updates

---

## Getting Started

### Prerequisites
- Python 3.7+
- Google Colab (recommended) or Jupyter Notebook
- Chrome browser (for Selenium)

### Installation
```bash
# Install required packages
pip install selenium pandas transformers sentencepiece sacremoses google-cloud-translate
```

### Setup (Google Colab)
```bash
# System setup for Chrome driver
apt-get update
apt install chromium-chromedriver
cp /usr/lib/chromium-browser/chromedriver /usr/bin
```

## Data Output

### Food Nutrition Data
- **24 Food Categories** across multiple languages
- **Nutritional Information**: Energy, Protein, Carbohydrates, Fats, etc.
- **Food IDs**: Unique identifiers for each food item
- **Category Classification**: Organized by food groups

### Contact Directory Data
- **Rotary Clubs**: 12 pages of club information
- **Travel Agents**: 105+ pages of agent listings
- **Contact Details**: Names, emails, phone numbers
- **Language Support**: Multi-language name extraction

### Building Management Data
- **Building Records**: 42,000+ building entries
- **Property Information**: Building names, organizations, ownership
- **Large-Scale Processing**: Checkpoint-based data collection
- **Government Database**: Official Hong Kong building management data

## Technical Features

### Modular Architecture
- **Reusable Classes**: Clean, maintainable code structure
- **Error Handling**: Comprehensive exception management
- **Language Support**: Multi-language text extraction
- **Data Validation**: Quality checks and data cleaning

### Performance Optimization
- **Headless Browsing**: Faster execution without GUI
- **Efficient Scrolling**: Custom scroll functions for dynamic content
- **Timeout Management**: Optimized wait times
- **Memory Management**: Proper resource cleanup

### Data Processing
- **Pandas Integration**: Advanced data manipulation
- **CSV Export**: Structured data output
- **Translation Services**: Google Cloud Translation API
- **Data Merging**: Intelligent DataFrame concatenation

## Use Cases

- **Research**: Academic and commercial data analysis
- **Business Intelligence**: Market research and competitor analysis
- **Contact Management**: Lead generation and directory building
- **Nutrition Analysis**: Food database creation and analysis
- **Language Processing**: Multi-language text extraction and translation
- **Property Management**: Building database creation and property analysis
- **Government Data**: Public sector information extraction and analysis
- **Real Estate**: Property ownership and management data collection

## Customization

Both projects are designed for easy customization:
- **URL Modification**: Change target websites
- **Data Field Addition**: Extract additional information
- **Language Support**: Add new language patterns
- **Output Format**: Modify CSV structure or add new formats

## Notes

- All scraping is performed in headless mode for efficiency
- Screenshots are automatically captured for documentation
- Data is exported in UTF-8 encoding for international character support
- Error handling ensures robust execution even with network issues

## Contributing

Feel free to fork this repository and submit pull requests for improvements or additional scraping solutions.

## License

This project is open source and available under the MIT License.
