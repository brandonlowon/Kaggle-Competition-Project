Here is where you include:
  - Background on your code files
  - How to run your code, guide to install any additional packages
  - Results, interpretation and reflection
  
  
  ### Background on Code Files
  The train.csv is the training data that will be preprocessed and cleaned for our models to use in this project. 
  Once the model is trained we will fit the model with the preprocessed and cleaned test set of data and our final output for the competition is our submission.csv.
  The submission.csv contains my model's predictions for if a given survivor survived or not.
  
  Project Titanic.ipynb is the jupyter notebook that will be used to run the entire code line to produce the results and detail my findings.
  
  ### How to Run
  
  For sklearn
  ***
  pip install -U scikit-learn
  
  For Pandas
  ***
  pip install pandas
  
  For seaborn plots
  ***
  pip install seaborn
  
  For numpy
  ***
  pip install numpy
  
  For mglearn
  ***
  pip install mglearn
  
  ## Conclusion
  ### What types of people were likely to survive the Titanic?
  
  Results from the visualization section of our report show 
- Gender was a significant indicator in determine if a passenger survived as over 70% of the females survived where as less than 20% of the males survived.
- Small sample size were if you are a person of royal background i.e having titles such as Sir, Lady, or Countess you had a 100% chance of surviving the wreck.
- Only significant indicator for age group was for individuals aged 0-5 years had just under 70% chance of survival.
- Persons belonging in First class had double the chance over persons belonging in the lowest class.

  ### Results
  From our research proposal, our goal was to compete in the Titanic Machine Learning Competition and to be able to successfully predict results from my trained model. With my results submitted, I achieved a score of 0.77272 which means my model was able to predict 77.3% of the passengers from the test set correctly. I believe these results to be quite excellent for a beginner Data Scientist/Machine Learning designer as I still have less than four months of experience. With my score I placed in the top 61% of all competitors. The model I concluded to be my best performing one is the Gradient Boosting Classifier as it scored the highest accuracy amongst the chosen three after I hypertuned the parameters. Using methods developed from assignments during the semester, I used cross-validation during the initial running of my models with no parameters set for any of them. A summary of those results can be shown below:

#### Scores Before Grid Search 
***
| Model | Training Score | Validation Score | 
| :- | -: | -: |
| RandomForestClassifier | 0.947 | 0.809 |
| GradientBoostingClassifier | 0.904 | 0.850 |
| SVC | 0.837 | 0.814 |
| LogisticRegression | 0.818 | 0.810 |
| GaussianNB | 0.780 | 0.761 | 


| Model | Accuracy | 
| --- | -: |
| GradientBoostingClassifier | 82.68 | 
| GaussianNB | 81.01 |
| SVM | 79.89 |
| LogisticRegression |79.89 |
| RandomForestClassifier | 78.77 |

#### Scores After Grid Search 
***
| Model | Training Score | Validation Score | 
| :- | -: | -: |
| GradientBoostingClassifier | 0.904 | 0.850 |
| SVC | 0.837 | 0.814 |
| RandomForestClassifier | 0.947 | 0.809 |

| Model | Accuracy | 
| --- | -: |
| GradientBoostingClassifier | 82.68 | 
| RandomForestClassifier | 81.56 |
| SVC | 56.42 |

With the grid search, we can see that the accuracy of our RandomForestClassifier model improved by almost 3 points where as our SVM model was improperly tuned as the accuracy dipped almost 25 points.

After performing the grid search for our top three models, I included a Precision-Recall Curve for our RandomForest model to find better thresholds for high recall results. However it seems that for this problem and looking at our confusion matrix with the adjust threshold obtained from the precision-recall curve we produced 50% more True positive results (survived) but an unacceptable amount of false positives as well. Default threshold : 55 true positive and 8 false positives, Adjusted threshold: 75 true positives and 77 false positives.

## Reflection
I think my report here accurately followed my project proposal. I was able to submit a successful submission to Kaggle and achieve an acceptable personal score for the purposes of this project and problem set. However one section I will discuss is the precision-recall curve. Comparing the graph I obtained with the one used in Lab 3 my results were more inaccurate after retrieving a threshold value for my confusion matrix for the RandomForestClassifier. This has been an excellent learning opportunity and I am glad I selected this for my machine learning project for this class. From this project I learned that preprocess of the data is just as important as the fine-tuning of the models as cleaning and correlating your features together can produce accurate scores from your model. I would like to thank Dr. Yves Pauchard for beling an excellent professor and role model for my first class in Machine Learning!

