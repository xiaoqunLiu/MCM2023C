## Entropy

The more we know about Wordle, the more "information" we want to get with each guessing attempt. In other words, if I eliminate more words in a single attempt, the more likely we are to win the Wordle game with fewer attempts.

An intuitive conclusion in information theory is that the more information we have about a situation, the less likely we are to encounter it. So how do we measure the expectation that a word will give us information? Information entropy helps us explain the relative amount of information that a word can give us.

The formula of information entropy is defined as follows:
$$
EN=-\sum_{i=1}^n P\left(x_i\right) \log p\left(x_i\right)
$$
Where $P$ is defined as the probability of a certain color combination, and $p$ is defined as the proportion of the number of words left by the information provided to the total words

We found that at the first guess, the information entropy of each word was the same regardless of the answer to the riddle, which can be used as an indicator to measure the properties of a word. Let's use the code to compute the entropy of information: