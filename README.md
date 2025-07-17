# Python News

Python News is a Python terminal application that allows you to read the latest news from major Brazilian media websites using web scraping with Beautiful Soup. The project offers a simple and interactive interface to access up-to-date news directly from your terminal, with options to add or remove sources and open full articles in your browser.

## Features

- **Fetches news from multiple sources:** Supports major sites like Globo, Veja, R7, and CNN Brasil.
- **Automatic updates:** News is refreshed in the background every few seconds.
- **Interactive menu:** Easily browse news, switch pages, and open articles directly from your terminal.
- **Manage sources:** Add or remove news sources according to your preferences.
- **Persistent data:** Keeps your preferences and previously fetched news across sessions.

## How it works

The main script (`asimov_news.py`) initializes the application, manages the menu, and handles user interaction. News scraping is handled by the `Site` class in `scraping_sites/site.py`, with a separate thread fetching updated news periodically. Data is stored locally using pickle for persistence.

## Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yagosamu/python_news.git
   cd python_news
   ```

2. **Create a virtual environment (optional, but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   Or manually install:
   ```bash
   pip install beautifulsoup4 requests pytimedinput
   ```

4. **Directory structure:**
   ```
   asimov_news/
   ├── asimov_news.py
   └── scraping_sites/
       └── site.py
   ```

## Usage

Run the main script:

```bash
python python_news.py
```

### Menu Options

- **1. Latest News:** View the most recent news from your selected sources.
    - Use `P` for next page, `A` for previous page, `L` to open an article in your browser, `V` to return to the menu.
- **2. Add Site:** Add more news sources to your feed.
- **3. Remove Sites:** Remove sources you no longer want to follow.
- **4. Exit:** Close the application.

## Requirements

- Python 3.8 or higher
- Modules:
  - `requests`
  - `beautifulsoup4`
  - `pytimedinput`

*Install them with the command:*
```bash
pip install requests beautifulsoup4 pytimedinput
```

## Notes

- The project is intended for educational purposes and may break if the structure of the source websites changes.
- News is fetched using web scraping; please use responsibly and respect each site's terms of use.
- The application stores news and preferences using pickle files (`news` and `sites`) in the project directory.

## Customization

To add more sources, edit the `Site` class in `scraping_sites/site.py` and include the parsing logic for the new website.


---

Created by [yagosamu]
