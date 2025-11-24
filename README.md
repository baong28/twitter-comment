# twitter-comment

## I. Concept

###  Twitter Sentiment Analysis Dataset:
#### This is an entity-level sentiment analysis dataset of social network comments on Twitter. Given a message and an entity, the task is to judge the sentiment of the message about the entity.
#### This is a multi-class classification problem, which simply means the dataset has more than 2 classes (binary classifier). The three classes corresponding to sentiments:

```
     -1 - Negative
      0 - Neutral
      1 - Positive
```
#### We regard messages that are not relevant to the entity (i.e. Irrelevant) as Neutral.

### >> Check out video below <<

![](twitter-gif.gif)

## II. User Guide

###  Step 1: Get data

#### DataFrame file > 25MB, so the file need to be zipped 
```
Unzipped file DataFrame.zip --> to get file DataFrame.sav 
```

###  Step 2: Get a virtual environment
```
python -m venv "venv_name"
```

```
venv_name\Scripts\activate
```

###  Step 3: Install required libraries 
```
pip install -r requirements.txt
```

###  Step 4: Run the App
```
streamlit run app.py
```

## III. Project Structure
```
├── requirements.txt          # List of all required libraries
├── train.py                  # Script to train the model using Kaggle dataset (twitter-training.csv)
├── test.py                   # Script to test model accuracy with dataset (twitter-validation.csv) → outputs 'final_result.csv'
├── app.py                    # Script to run the Streamlit app to display model results
├── final_result.csv          # Prediction results:
│                             #   - Sentiment_test: predicted values
│                             #   - Sentiment: true values
├── DataFrame.zip             # Contains DataFrame.sav — unzip this file after cloning the repository (see User Guide Step 1)
├── model1.sav                # Saved trained model
└── twitter-practices.ipynb   # Jupyter Notebook for practice
```


