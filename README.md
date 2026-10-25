# Student Risk Prediction

Analysis code for the manuscript *Predicting Student Academic Risk in a Subsequent Mathematics Course from Prerequisite and In-Course Assessment Records*.

The notebook `Student_Risk_Prediction.ipynb` builds and evaluates models (Logistic Regression, Random Forest, Gradient Boosting) that flag students at risk of a failing or near-failing grade in a subsequent mathematics course, using prerequisite-course and in-course assessment marks. Batches 22-24 form the development set (stratified 5-fold cross-validation) and Batch 25 the temporally separate validation set.

## Data

The study used anonymised course-evaluation records. They contain no names or registration numbers and **are not included** in this repository, because they are student records. Students appear only as an anonymised `student_code`. See the data availability statement in the manuscript for access.

Expected layout of `data/` (see `COHORT_CONFIG` in the notebook):

```
data/batch22_prerequisite_*.xls   data/batch22_subsequent_*.xls
...
data/batch25_prerequisite_*.xls   data/batch25_subsequent_*.xls
```

## Running

```
pip install -r requirements.txt
jupyter notebook Student_Risk_Prediction.ipynb
```
