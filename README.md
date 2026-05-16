# Document Clustering and Topic Modelling
## ABC News Headlines Dataset

---

## Package Requirements

Install all required packages using this single command:

pip install pandas numpy scikit-learn nltk matplotlib seaborn wordcloud gensim

### Full Package List
| Package      | Purpose                                      
| 
| pandas       | Data loading, CSV reading, Series operations |
| numpy        | argmax for dominant topic extraction         |
| scikit-learn | TfidfVectorizer, CountVectorizer, KMeans,    |
|              | LDA, TSNE, silhouette_score                  |
| nltk         | Stopwords, WordNetLemmatizer                 |
| matplotlib   | All plots and visualizations                 |
| seaborn      | Scatterplot and countplot                    |
| wordcloud    | Word cloud generation per topic              |
| gensim       | Installed in notebook (pip install gensim)   |
| re           | Built-in Python — no install needed          |

### NLTK Downloads
Run this once before executing the notebook:

import nltk
nltk.download('stopwords')
nltk.download('wordnet')

---

## Dataset Required
- File name : abcnews-date-text.csv
- Place this CSV in the same folder as the notebook
- Without this file the notebook will not run

---

## Run Instructions

### Option 1 — Google Colab (Recommended)
1. Go to https://colab.research.google.com
2. Upload PRML_PROJECT.ipynb
3. Upload abcnews-date-text.csv to the Colab session:
   - Click the folder icon on the left sidebar
   - Click upload and select abcnews-date-text.csv
4. Run the following install command in the first cell:
   pip install wordcloud gensim
   (pandas, numpy, sklearn, matplotlib, seaborn, 
    nltk are pre-installed on Colab)
5. Go to Runtime > Run All
6. Wait for all cells to finish executing top to bottom

### Option 2 — Local Jupyter Notebook
1. Download and place these two files in one folder:
   - PRML_PROJECT.ipynb
   - abcnews-date-text.csv
2. Open terminal in that folder
3. Run:
   pip install pandas numpy scikit-learn nltk 
   matplotlib seaborn wordcloud gensim
4. Then run:
   jupyter notebook
5. Open PRML_PROJECT.ipynb in the browser
6. Go to Kernel > Restart & Run All
7. Wait for all cells to finish top to bottom

---

## Execution Order Inside Notebook

Step 1 — Data Loading
         Read CSV, check shape, remove nulls and duplicates

Step 2 — Text Cleaning
         Lowercase, remove punctuation using re library

Step 3 — NLTK Preprocessing
         Remove stopwords, apply lemmatization

Step 4 — TF-IDF Vectorization
         Build document-term matrix for K-Means input

Step 5 — K-Means Clustering
         Elbow curve (k=21 to 34)
         Silhouette scores (k=2 to 69)
         Final model with k=19

Step 6 — t-SNE Visualization
         2D scatter plot of 19 clusters

Step 7 — Count Vectorization
         Build count matrix for LDA input

Step 8 — LDA Topic Modelling
         10 topics, top words per topic printed

Step 9 — Visualizations
         Word clouds per topic
         Topic distribution countplot
