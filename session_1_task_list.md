# Introducing `scikit-learn` tutorial task list:

Please find in this document a list of tasks for you to explore. There is no formal requirement of completing anything specific. Instead, these are designed to guide you through the session and provide you with familiarity for the upcoming session and your future data science related studies.

## Data representation in `scikit-learn`
* What does the pairwise seaborn plot represent, and how do you interpret it?
* What would happen (what accuracy score and why) if you were to not drop the `species` array and still perform prediction with that data?

---
## Classification on digits
* Try changing the random seed (`random_state`) to 10 different values and note down your results in a dictionary with key: `random_state`, value: `accuracy_score`.
* Experiment with re-running the same model also on the same data (with fixed `random_state`)
* What can you conclude about the dataset and modelling variability based on these results?

### Extension
* Walk through a tutorial on the operation of one (or more) of the following:
  * [Support Vector Machines](https://jakevdp.github.io/PythonDataScienceHandbook/05.07-support-vector-machines.html)
  * [Random Forests](https://jakevdp.github.io/PythonDataScienceHandbook/05.08-random-forests.html)
* Implement a more sophisticated model such as the SVM or RF as referenced and repeat the task above.
---
