![HumBug](https://raw.githubusercontent.com/ikiskin/UNIQ-deepmind/master/data/pics/humbug-logo.png)
# Mosquito detection `scikit-learn` tutorial task list:

Please find in this document a list of questions designed to get you to think about the problem at hand, and to help you log how changing components of the whole pipeline affect the overall performance of the system. The questions are designed to be covered in order, and are fully contained within the original notebook. They are numbered and repeated here for your convenience. Please start a new document using your editor of choice (Markdown, Google Doc, Overleaf, Word, anything else you like), and write down your responses to the following questions below. Where you are asked to complete the code, simply note down which models you use (or copy paste your completed cell from the notebook). 

It should be noted that you can go into great depth into any of these particular questions: you are free to choose which points interest you more and are worth exploring in depth to your liking.

---

**1. Visualise the difference between a data sample (or the full training dataset) before and after applying the StandardScaler transform. What does it do? You may use `plot.imshow()` to help you with visualisation. You may also access the variables stored by `StandardScaler` with `scaler.mean_` and `scaler.var_`**


---


**2. Complete the code section where appropriate to instantiate a model, and predict over data normalised with the scaler as previously introduced. You can experiment by removing the normalisation/data transform and examining the effect it has on the outcome.**

For this problem, you might want to consider using one of the following:
* [Random Forest classifier (RF)](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
* [Gaussian Naive Bayes classifier (GNB)](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html)
* [Support Vector Machine (SVM)](https://scikit-learn.org/stable/modules/svm.html)

---

**3. Run the performance metrics below, noting down and saving the following figures for a short report:**
* Number of samples of `'background'` audio
* Number of samples of `'mosquito'` audio
* Accuracy score
* F1-score, Precision and Recall as seen from the `classification_report`
* Plot of precision against recall

--- 
**4. Going back through the notebook, see if you can make alterations to the code to improve upon baseline classification performance as given in the notebook. You might consider changing the following:**
* Type of classifier used
* Data normalisation
* Feature settings:
  * Number of MFCC features
  * Default parameters of MFCC transform
  * Compressed feature space e.g. PCA
  * Entirely different feature settings: see [Librosa's feature library](https://librosa.org/doc/main/feature.html). You can choose a combination of these stacked into a single array. This would be similar to how [OpenSMILE](https://audeering.github.io/opensmile/about.html) operates.

**Please be aware of the number of samples your feature extraction will produce, as it will generally be easier to achieve better classification on longer windows, as it corresponds to having to get fewer predictions per unit time correct.**

For this task, you may want to save your results to a dictionary containing appropriate metrics, and you could consider using `plt.savefig()` to save the precision-recall curves.

---
**5. Experiment with changing the contents of the test set, as determined in the code. What happens to the classification performance, and what does this tell us about the practice of creating datasets?**

If you do not have enough time to change and re-run code, what do you expect might happen, and what best practices should we apply to avoid "cherry picking" results with a particular dataset split?
