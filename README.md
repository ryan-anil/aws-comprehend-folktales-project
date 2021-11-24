# aws-comprehend-folktales-project : An Investigation of AWS Comprehend and its Biases

Contains instructions and example code required to perform natural language processes using the AWS Comprehend machine learning service in Python.

# An Introduction
Due to the path-dependent and ever-evolving nature of machine learning, we seek to uncover the nuances and potential biases within the service. Understanding such weaknesses is an important component of any data science project. The many real-world applications of Comprehend have the potential to severely underperform in the presence of bias, leading to poor analysis and weak results that can then be used throughout daily life, having potentially numerous ripple effects. 

One common bias within machine learning models is a lower confidence in processing non-Western (e.g. American, Western European) information. Within the scope of NER, this may include processing names, cities, and other proper entities. Because of this topic’s important implications for Comprehend’s outcomes, we feel that this is a relevant and necessary investigation.

In this investigation, we seek to uncover a potential [bias](https://www.technologyreview.com/2018/12/02/138843/ai-has-a-culturally-biased-worldview-that-google-has-a-plan-to-change/) within NER. We proceed by analyzing Comprehend’s response to excerpts from a text dataset of folk tales that originate from the Arabian Peninsula, China, England, Germany, India, and Russia. We then compare NER’s analysis of the English tales (which contain a much higher proportion of names commonly seen in Western culture) to all others. 

Our approach uses a variety of AWS services. First, we use S3 buckets to store and organize our folk tales. We utilize Sagemaker to read in the text data, conduct exploratory data analysis, and our assessment of the NER service. Finally, we use Comprehend to analyze the folk tales for named entities. See below for architecture diagram. 

![image](https://user-images.githubusercontent.com/91302295/143170372-a95ca5fe-518e-4c91-914c-a999cae4dc75.png)


# Contents of our Repo

This section contains an outline and description of the files and folders in our repo and the purpose of each one of them.

## ner
