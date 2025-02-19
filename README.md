# ICS Search Engine

Welcome to the **ICS Search Engine**! This web-based search engine is built from scratch to efficiently handle up to two thousand documents or web pages from the School of Information and Computer Science (ICS) at the University of California, Irvine (UCI). Powered by Python's Flask framework, this project leverages advanced Information Retrieval techniques, including text processing, indexing, and ranking algorithms. Additionally, it integrates the OpenAI API for automatic summary generation, enhancing the relevance and user experience of search results.

## Features

- **Text Processing:** Utilizes NLTK to perform tokenization and stemming on documents.
- **Indexing:** Implements an inverted indexer to store processed documents, mapping terms to the documents they appear in, alongside their TF-IDF scores and importance.
- **Ranking:** Ranks documents based on their TF-IDF scores to provide a list of top search results.
- **Web Scraping:** Uses the BeautifulSoup library to parse HTML and extract useful information.
- **Summary Generation:** Employs OpenAI's GPT-3 model to generate a summary of search results.
- **Flask Web Application:** Hosted on a Flask server, handling GET and POST requests and rendering a simple and intuitive user interface.

## Installation

To run this project locally, follow these steps:

### Clone the Repository:
```bash
git clone https://github.com/ajajoo11/ICS_SearchEngine_UCI.git
cd ICS_SearchEngine_UCI
```

### Install Required Modules
Ensure you have the following Python modules installed:

- `nltk`
- `bs4`
- `re`
- `os`
- `json`
- `tqdm` (timer)
- `openai` (for OpenAI API)
- `timer`

You can install them using pip:
```bash
pip install nltk beautifulsoup4 tqdm openai
```

## File Structure
Once you unzip the submission file, you should see the following files:

- `indexer.py`
- `Searcher.py`
- `gui.py`
- `README.txt`
- `templates/` folder containing `index.html`

## Building the Indexer

1. Ensure you have the `DEV` folder in the same directory as `indexer.py`.
2. Run `indexer.py` using Python 3.2:
   ```bash
   python3.2 indexer.py
   ```
3. A progress bar will display the runtime.
4. The program should take 15-16 minutes to complete and will generate the following files in the same directory:
   - `finalreverseindexer.txt`
   - `index2.txt`
   - `index3.txt`
   - `DocIDS.json`

## Running the Search Engine Web GUI

1. Run `gui.py` using Python 3:
   ```bash
   python3 gui.py
   ```
2. The console will display Flask server information.
3. Open the provided link in a web browser. For example, if the console prints:
   ```
   Running on http://127.0.0.1:5000
   ```
   Open `http://127.0.0.1:5000` in your browser.
4. The web GUI will allow you to enter queries, view search results, and check the time taken for retrieval.

## Additional Features

- **Web GUI:** A user-friendly interface for searching and viewing results.
- **Duplicate Page Detection:** Eliminates duplicate pages to enhance result quality.
- **Summarization:** Generates summaries of search results using the OpenAI API. Clicking the **summary** button takes 2-3 seconds to generate a short summary.

---

Enjoy using the ICS Search Engine!

