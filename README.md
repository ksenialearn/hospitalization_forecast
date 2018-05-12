Hospital admissions are a large driver for healthcare costs. In the U.S., about 30% of the
national health expenditures are attributed to hospital care. On a patient level, this cost is
high and can be catastrophic to both health and financial wellbeing.

The goal of this project is to build a model predicting patient hospitalization. 


The dataset is the CMS Linkable 2008–2010 Medicare Data Entrepreneurs’ Synthetic Public
Use File (DE-SynPUF). (~5GB of data)

Random Forest model resulted in the best performance in this project.

I chose to use out-of-bag error for error estimation in the Random Forest, which was a
more efficient way to tune hyperparameters compared to cross-validation. Out-of-bag estimate
of performance improvement evaluates predictions on observations that were not used in the
base learner, thus avoiding the need for an independent validation set.

I used Grid Search algorithm for determining the optimal hyperparameters. We used recall
as the scoring and evaluation metric. The best Random Forest model included 200 estimators and 50 minimum
samples per leaf. Test accuracy was 95.48% and recall was 66.96%, compared to the baseline model’s 87.28%
accuracy and 15.88% recall.


