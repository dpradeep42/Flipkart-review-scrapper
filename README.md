# Flipkart-review-scrapper

A Flask web app that searches Flipkart for a product, opens the first result and scrapes customer reviews (name, rating, comment heading and comment) with BeautifulSoup. The reviews are shown in a results page and also saved to a CSV file named after the search term. Built as a learning project and set up for Heroku deployment.

## Tech stack

- Python 3.9
- Flask, Flask-CORS
- BeautifulSoup 4, requests
- Gunicorn (Heroku `Procfile`)

## How to run

```bash
pip install -r requirements.txt
python app.py
```

Open the local URL Flask prints, enter a product name and submit the form.

## Structure

- `app.py` - Flask routes: `/` (search form) and `/review` (scrape and show results)
- `templates/`, `static/` - HTML templates and styles
- `*.csv` - sample review files saved from earlier searches
- `Procfile`, `runtime.txt` - Heroku configuration

## Notes

Scraping depends on Flipkart's page markup at the time it was written and may need updating if the site layout has changed.
