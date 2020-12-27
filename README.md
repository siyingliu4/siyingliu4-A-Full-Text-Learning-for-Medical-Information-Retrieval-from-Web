# A Full-Text Learning for Medical Information Retrieval from Web
This readme file is written by one of the team members Gongna.


## FOLDER STRUTURE
### Preprocessing
	00_preprocessing.jpynb - Python code for the whole preprocessing	
	doc_dump.xlsx          - Documents in a column-separated format: ID, TEXT
	nfdump.xslx            - Query in a column-separated format: ID, TEXT
	stopword.xlsx 		   - A given stopword list
	
### Basic SVM Model
	TF-IDF Schema 0-5      - Python code for 6 different TF-IDF schemas.
	df_doc_pre.xlsx        - Preprocessed documents file generated from basic model
	df_query_pre.xlsx      - Preprocessed query file generated from basic model
	dictionary.csv         - Term dictionary of all documents
	document_frequency.csv - Document frequency in a column-separated format: tf, term
	all2-1-0.qrel.xlsx     - Provided relevence judgment for 3 levels in total: direct links (2), indirect links (1), marginally relevant and others (0, not in the files)
	
### Speed Up Models
	00_Pre-clustering_single_path.ipynb       - Python code for pre-clustering(single path) speed up model
	01_Pre-clustering_K-means.ipynb           - Python code for pre-clustering(K-means) speed up model
	02_Random projection.ipynb                - Python code for random projection speed up model
	03_Tiered Index.ipynb                     - Python code for tiered index speed up model
	04_pre-clustering+Random_Projection.ipynb - Python code for combining the random projection and pre-clustering
	q_tfidf2000.csv                           - Best query TFIDF vetor results of random projection, used for combining the random projection and pre-clustering
	d_tfidf2000.csv                           - Best document TFIDF vetor results of random projection, used for combining the random projection and pre-clustering
	new_doc1-8.csv                            - The exported document vector results of all random projections
	new_q1-8.csv                              - The exported query vector results of all random projections

### Results Comparison
	Speed_up_testing_results - The raw testing results of all speed up models
		comparison           - Overall result comparison of basic model and 3 speed up models (including retrieval time for one query, MAP and NDCG).
		K-Means              - Pre-clustering with K-means result comparison
		Single_Path          - Pre-clustering with Single_path result comparison
		RP_similarity        - Retrieval time comparison of cosine similarity and hamming similarity in random projection
		RP_map               - MAP comparison with different thresholds in random projection
		RP_ndcg              - nDCG comparison with different thresholds in random projection
		Tiered_tiers         - Tiers result comparison in Tired index model
		Tiered_p             - p value result comparison in Tired index model 

### Time Testing
	00_time_test.ipynb    - Python code of time comparison for all models by take average time of random 200 queries.
	The rest are imported files to run time_test model. Detailed description could be found from above
	
### Usage
All refered files, parameter setting are stored in corresponding folder and source code, so every piece of code could be tested directly by simply clicking 'run'.
