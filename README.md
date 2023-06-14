Find similar news from the database using cosine similarity.
## The process of assigning clusters to the news articles in the database is as follows (Training): 
1. Preprocess the news articles.
2. Convert the news articles into embeddings using SentenceTransformer.
3. Reduce the embeddings' dimensionality using PCA.
4. Assign clusters to the articles in the database.

## The process of filtering similar news articles from the database based on the input news article (Inference):
1. Preprocess the input news article.
2. Convert the news article into embeddings using SentenceTransformer.
3. Reduce the embeddings' dimensionality using PCA.
4. Predict the cluster of the news article.
5. Filter the news articles in the database belonging to the predicted cluster. This reduces the number of news articles for which the cosine similarity needs to be computed.
6. Compute the cosine similarity between the input article and the articles in the database filtered in step 5.
7. Return the top 'n' similar articles with highest cosine similarity.
