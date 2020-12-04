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
## Setup

### Clone

Clone this repo to your local machine using `https://github.com/Shrivallabha/SentimentAnalysisModel.git`

### Deploying Streamlit App 

The pipeline uses [Streamlit](https://www.streamlit.io/) for allowing the user to select a file with URLs. The app directly interacts with the aws built components and provides a GUI to run the pipeline without the need for the end-user to manually trigger the pipeline.

The Python code for this app can be found at `streamlit_webapp/app.py`.
> Install required libraries

```
pip3 install streamlit
pip3 install boto3
pip3 install pandas
```

> Run `app.py`

Run the WebApp by running `streamlit run app.py`.

### Building Docker

#### Download the TensorFlow Serving Docker image and repo
docker pull tensorflow/serving

git clone https://github.com/tensorflow/serving
#### Location of demo models
`/path/to/my_model/`

#### Start TensorFlow Serving container and open the REST API port
```
docker run -p 8501:8501 \ 
--mount type=bind,source=/path/to/my_model/,target=/models/my_model 
-e MODEL_NAME=my_model -t tensorflow/serving
```

#### Results => { "predictions": [4.5] }
