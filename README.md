# Clustering Task

Build a robust company classifier for a new insurance taxonomy.

Accept a list of companies with associated data:
+ Company Description
+ Business Tags
+ Sector, Category, Niche Classification

# Approach

I have studied the provided data. Since it is unlabled, I decided to go with clustering, to try to separate the companies and see how they naturally align. I started reaserching different methods to do so, and I have decided to go with hierarchical clustering in the beginning. 

I chose hierarchical clustering since I wasn't sure on how many different clusters I want, because each company can have more that one insurance taxonomy label.

For the sentences embeddings i am using SentenceTransformer with "all-MiniLM-L6-v2" model, where the dimention of an embedding is 384. Then I am doing PCA to reduce the dimention to 150.
I am doing this for each column of the dataframe, then I am combining the different results and try a clusterisation

1. Data Preprocessing
     + I am removing the following, because they do not give me useful information for the insurance taxonomy and add noise to my data.
       + Stop words (using standard nltk library)
       + Place names (using a NER model)
2. Embeddings
3. Clustering 
