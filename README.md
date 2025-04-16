# 📰 HackerNews Web Scraper

A Python-based web scraper that collects the relevant posts from [Hacker News](https://news.ycombinator.com/) using `Selenium`, `BeautifulSoup`, and `Requests`. Compiles detailed results, it implements a two-phase system: first it identifies relevant URLs and then performs deep scraping with metadata, saving results in HTML, SQLite and/or CSV.

---

## 🚀 Features (Planned)

- Scanning: Search with Selenium in real time.
- Extraction: Complete download of the content of each link.
- Interactive CLI for customized searches.
- Support for automatic pagination and result limiting.
- Download of full HTML with Selenium.
- Scrapes top stories from Hacker News.
- Parses HTML efficiently using BeautifulSoup.
- Can be extended for pagination or deeper content.
- Includes a test suite to validate core functionality.
- Audible notification at the end of the process.

---

## 🧪 Tests

- Fixtures for temporary databases.
- HTTP response mocking.
- Scraping validation and URL processing.
- Execute tests with:

```bash
> pytest
```

## 📦 Installation

### 1. Clone the repository

```bash
> git clone https://github.com/samhernandezcdev/hn-web-scraper.git
> cd hn-web-scraper
```

### 2. Create and activate a virtual environment
On macOS/Linux:
```bash
> python -m venv venv
> source venv/Scripts/activate
```

On Windows:
```bash
> python -m venv venv
> venv\Scripts\activate
```

### 3. Install dependencies
```bash
> pip install -r requirements.txt
```

> Make sure you have Chrome and **ChromeDriver** installed and available in your system PATH.

## 💻 How to run it?
```bash
> python project.py
```

### Example:
```markdown
> Enter your search term: "Python Web Scraping"
> How many elements do you want to scrape?: 50
> [PROCESSING] Searching in HackerNews...
> [PAGINATION] Page 1/3 | URLs found: 15/50
> [RECOPILING] Scrapping individual URLs...
> [PROGRESS] ████████████████████ 70% | 35/50
> [STORING] Saving the files...
    - 50 records in db/2025-04-16_hn_scrape.db
    - HTMLs in scrapes/2025-04-16_Python_Web_Scraping/
> [COMPLETED] 3.2 MB of data collected (00:02:17).
🔔 (sound notification).
```