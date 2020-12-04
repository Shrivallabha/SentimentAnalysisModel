# SentimentAnalysisModel
Sentiment Analysis for earnings transcript using the pre-trained model

**Team Members**<br />
Prajwal Mylar <br />
Pramod Pai <br />
Shrivallabha Kulkarni <br />

##### Web hosting - Streamlit Application<br />

## Table of Contents

- [Introduction](#introduction)
- [Setup](#setup)
- [TestCases](#testcases)

## Introduction
Sentiment Analysis for already scraped and anonymized data of companies earnings calls, Which returns a sentiment score.

#### Architecture 

![alt text](https://github.com/Shrivallabha/SentimentAnalysisModel/blob/main/SentimentAnalysisArchitecture.png)

---

### Clone

Clone this repo to your local machine using `https://github.com/Shrivallabha/SentimentAnalysisModel.git`

### Deploying Streamlit App 

The pipeline uses [Streamlit](https://www.streamlit.io/) for allowing the user to upload a file with URLs. The app directly interacts with the built components on AWS and provides a GUI to run the pipeline without the need for the end-user to manually login to AWS Account and trigger the pipeline.

The Python code for this app can be found at `streamlit_webapp/app.py`.
> Install required libraries

```
pip3 install streamlit
pip3 install boto3
pip3 install pandas
pip3 install configparser
```

> Run `app.py`

Run the WebApp by running `streamlit run app.py`.
