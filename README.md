# ICS Website Search Engine

## Overview
This is a search engine built specifically for indexing and retrieving content from the University of California, Irvine's ICS websites. The system processes web pages, indexes their content, and allows users to search for relevant information through a web interface.

## Features
- **Indexing System:** Processes and stores web page data for efficient retrieval.
- **Search Functionality:** Supports keyword-based search with ranking based on relevance.
- **Stopword Filtering:** Removes common words to improve search accuracy.
- **Boolean AND Matching:** Retrieves documents containing all query terms.
- **Summarization:** Uses OpenAI's API to generate summaries of retrieved pages.
- **Dark Mode Support:** UI includes a dark mode toggle for better accessibility.

## Files & Directory Structure
```
📂 project-root/
├── gui.py              # Flask-based frontend and search handling
├── indexer.py          # Processes and indexes web pages
├── searcher.py         # Retrieves and ranks search results
├── templates/
│   ├── index.html      # Frontend HTML template
├── finalreverseindexer.txt  # Merged index file
├── index2.txt          # Character position index
├── index3.txt          # Alphabet-wise index
├── DocIDs.json         # Maps document IDs to URLs
```

## Installation & Setup
### Prerequisites
Ensure you have Python 3 installed along with the following dependencies:
```
pip install flask nltk beautifulsoup4 tqdm openai requests
```

### Running the Project
1. **Run the Web Interface:** Since the indexer files have already been uploaded, you can directly run the GUI without indexing.
   ```
   python3 gui.py
   ```

2. **Access the Search Engine:** Open your browser and go to:
   ```
   http://127.0.0.1:5000/
   ```

3. **Perform a Search:** Enter a query in the search bar and retrieve ranked results.

### Important Note
🚨 **API Key Requirement:** The OpenAI API key is not included in this repository for security reasons. Before running the project, you must add your OpenAI API key in `gui.py` and `searcher.py` where required.

## How It Works
1. **Indexing (indexer.py):**
   - Extracts content from JSON web page files.
   - Tokenizes, stems, and assigns importance weights.
   - Generates index files (`finalreverseindexer.txt`, `index2.txt`, `index3.txt`, `DocIDs.json`).

2. **Searching (searcher.py):**
   - Processes user queries and removes stopwords.
   - Matches query terms using a boolean AND operation.
   - Scores and ranks search results.

3. **Frontend (gui.py & index.html):**
   - Handles user queries via Flask.
   - Displays search results and allows users to request page summaries.

## Future Improvements
- Implement phrase searching and wildcard support.
- Enhance the ranking algorithm with additional weighting factors.
- Improve UI/UX with more features like filters and categories.

---
Developed by Bhuvan Chandra

