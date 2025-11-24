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
├── requirements.txt          # Danh sách toàn bộ thư viện cần thiết
├── train.py                  # Script huấn luyện mô hình với dữ liệu Kaggle (twitter-training.csv)
├── test.py                   # Script kiểm tra accuracy với dữ liệu twitter-validation.csv → xuất 'final_result.csv'
├── app.py                    # Chạy ứng dụng Streamlit để hiển thị kết quả mô hình
├── final_result.csv          # Kết quả dự đoán: 
│                             #   - Sentiment_test: giá trị dự đoán
│                             #   - Sentiment: giá trị thật
├── DataFrame.zip             # Chứa file DataFrame.sav — cần giải nén sau khi clone repo (theo User Guide Step 1)
├── model1.sav                # Mô hình đã được huấn luyện và lưu lại
└── twitter-practices.ipynb   # Notebook Jupyter dùng để thực hành

```
