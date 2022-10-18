# Naive_bayers

**Team 5**

**Team members:** Nazar Kononenko, Anna Polova, Natalia Chaika

**Variant 0**



**Description:**
_________

This R program processes dataset of sentences written by three different authors and then can determine by whish of three authors a given sentence is written. It guesses the author correctly in 84% of cases.

![image](https://user-images.githubusercontent.com/91616531/196491409-4af0b2ac-8550-468b-ad7d-10888e1949e2.png)




**Conclusion:**
_______

- The prgram implement Multinomial Naive Bayer's classifier algorithm to detemine an author of the sentence. It is based on Bayer's theorem, by which the probability that author A a wrote given sentence (P(A|sentence)) equals to the probability of author A writing this sentence (P(sentence|A)) multiplied by probability of choosing author A out of three authors (P(A)) divided by probability of this sentene (P(sentence)). We only need to compare these probabilities to determine which author is more likely, so we can omit the denominator, which is unknown and common for every author. Then we split the sentence by words, so the probability that author A a wrote given sentence (P(sentence|A)) to the product of probabilities of words in this sentence being written by this author П(P(word|A)). Probability author A wrote this word P(word|A) is frequentistic, which is number of times this word was written by A divided by total number of words written by A in the training dataset.

-  Naive Bayer's classifier if fast has quite high precision in processing natural languages. However, it needs a lot of training data and a lot of filters to get better results. The biggest drawback of this method is the assumption of independence, while in reality there is correlation between usage of some words in one sentence. Also if some words from testing dataset do not exist in training data, the straightforward multiplication will give the probability of zero, so we needed to use additive smoothing technique 
