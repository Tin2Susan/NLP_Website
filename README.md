Job Ads Text Processing

This project processes ~750 job advertisement documents across four categories (Accounting_Finance, Engineering, Healthcare_Nursing, Sales). Each ad is a .txt file containing title, webindex, and description.

Tasks
Task 1 — Pre-processing

Tokenize descriptions with regex: r"[a-zA-Z]+(?:[-'][a-zA-Z]+)?"

Lowercase tokens

Remove: short words (<2), stopwords (stopwords_en.txt), hapax words (TF=1), and top-50 frequent words (by document frequency)

Save preprocessed ads and build vocab.txt:

Format: word:index (alphabetical order, 0-based)

Task 2 — Feature Representations

Generate document features from cleaned descriptions:

Count Vector → count_vectors.txt (#webindex,index:freq,...)

Embeddings (unweighted) → mean word vectors

Embeddings (TF-IDF weighted) → weighted averages

Outputs

outputs/vocab.txt

outputs/count_vectors.txt

outputs/doc_embeddings_unweighted.npy

outputs/doc_embeddings_tfidf.npy

