# We use nltk library for easy and accurate sentence splitting of the tweet
import nltk                 
nltk.download('punkt')

# I created a small sample file containing simulated tweets which may or may not containg profanity
# In reality we will be using real-world data which would be much larger in content. However, the below code should work nonetheless.
with open('tweets.txt', 'r') as file:
    tweets = file.read().replace('\n', '')


# Sample list of racial slurs, which is assumed to be decided beforehand
racial_slurs = ['f-word', 'n-word']

# Sentence splitting process
tweets_sentences = nltk.sent_tokenize(tweets)
print(tweets_sentences)
print(len(tweets_sentences))


# We use profanity_count to count the instances of profanity occuring in each sentence
profanity_count = [0] * len(tweets_sentences)
print(profanity_count)

for i in range(len(tweets_sentences)):
    for j in range(len(racial_slurs)):
        profanity_count[i] += tweets_sentences[i].count(racial_slurs[j])


print(profanity_count)


# We use profanity_degree to rate how profane a sentence is through some basic logical if-else ladder
profanity_degree = [None]*len(profanity_count)

for i in range(len(profanity_count)):
    if profanity_count[i] == 0:
        profanity_degree[i] = 'Normal Tweet'
    elif profanity_count[i] <= 1:
        profanity_degree[i] = 'Slightly Profane'
    elif profanity_count[i] <= 3:
        profanity_degree[i] = 'Profane'
    else:
        profanity_degree[i] = 'Highly Profane'

print(profanity_degree)