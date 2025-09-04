# RAOP Altruistic Request Success

#### Overview
This project replicates and extends findings from Althoff et al. (2014) on what drives successful altruistic requests on Reddit’s r/Random_Acts_of_Pizza (RAOP). We compare feature families (language vs. user reputation/behavior) using linear SVMs to predict whether a request receives a pizza.

#### Repository Contents
- assignment3_v2.pdf — Report (methods, results, discussion, comparison to Althoff et al.)
- Part1Code.ipynb — Code for Model 1 (N-grams): training + evaluation with linear SVM
- pizza_request_dataset.json: dataset
- read_dataset: notebook file to read in and process the dataset
  
#### Methods (Part 1 snapshot)
We trained Support Vector Machine (SVM) classifiers on four different feature families to isolate what drives success in altruistic requests:
1. Model 1 (N-grams): top 500 unigrams + top 500 bigrams as TF-IDF features → SVM
- Tests how phrasing and linguistic style matter.
2. Model 2 (Activity and Reputation): features capturing requester activity and credibility (e.g., account age, karma, comment/post history)
- Tests how trust and reputation signals matter.
3. Model 3 (Narratives): normalized counts of words from 5 narrative dictionaries (e.g., family, student, money, desire, job)
- Tests how storytelling and context matter.
4. Model 4 (Moral Foundations): normalized counts of words tied to 5 moral dimensions (care/harm, fairness, loyalty, authority, purity)
- Tests how moral reasoning in requests matters.

#### Key Takeaways
- User activity/reputation features (account age, engagement) outperform purely linguistic features for predicting success.
- N-gram models carry moderate signal; dictionary-based narrative/moral features are weaker without richer context.
- Best performance comes from behavioral/reputation signals, aligning with Althoff et al.’s conclusions.
