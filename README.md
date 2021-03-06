**Collect.py**

Collecting data from Twitter API.
I have collected the followers of 4 Indian cricketer: Virat Kohli, M S Dhoni, Suresh Raina, Rohit Sharma.
Collected 500 followers of these this four indian cricketers and stored them in user's dict using a new key called 'friends'. Created undirected Graph, adding each user and followers a node.
Stored the graph using pickle into a file named as graph.pickle.
Collected the tweets by querying the parameter as the screen_name of the users.
Stored the tweets using pickle into a file named as tweets.pickle.

**Cluster.py**

Loaded the graph stored in graph.pickle into a dictionary named graph.
Used Girman Newman Algorithm to find two clusters. The original graph is saved to network.png.
![Network](https://github.com/Arpit3697/Online-Social-Network-Analysis-CS579/blob/master/a4/network.png?raw=true)
Stored the clusters details using pickle into a file named as clusters.pickle.


**Classify.py**

Loaded the tweets stored in tweets.pickle into a dictionary named as tweets.
Downloaded the AFINN dataset for the analysis of raw data (tweets) whether the tweets about the users is positive, negative or mixed.
Tokenized the tweets into tokens and score the tokens on the basis of AFINN dataset.
If the tweet contains more score of positive words than negative words then the tweet belongs to the positive class.
If the tweet contains more score of negative words than positive words then the tweet belongs to the negative class.
And if the score of positive and negative words are equal then the tweet belongs to the mixed class.
Stored the results in the file named as classify.pickle.

**Summarize.py**

Collected the information using the results got from collect.py, cluster.py and classify.py. You can see the Summary and Positiveness and Negativeness of the tweet.
