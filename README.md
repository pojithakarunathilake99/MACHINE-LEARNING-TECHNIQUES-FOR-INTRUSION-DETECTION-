# Machine Learning Models for CIC-IDS-2018
## Dataset Source
https://www.kaggle.com/datasets/solarmainframe/ids-intrusion-csv
## Introduction
Machine learning is an artificial intelligence subfield that includes teaching machines to spot patterns in data and make judgements based on that data. It has several applications, including cybersecurity. Machine learning algorithms in cybersecurity can detect and prevent cyber risks like malware or phishing attempts.There are several ways in which machine learning can be used to improve cybersecurity:
1. Anomaly detection: Machine learning algorithms can be trained to recognize normal behavior 
patterns in a system and flag any deviations from that norm as potentially malicious. This can be used to 
detect cyber threats that might not be detected by traditional security measures.
2. Malware detection: Machine learning algorithms can be trained to recognize the characteristics of 
different types of malware and flag any suspicious files for further investigation.
3. Phishing detection: Machine learning algorithms can be used to identify phishing emails by 
analyzing the text and structure of the message, as well as the reputation of the sender.
4. Network security: Machine learning algorithms can analyze network traffic and identify unusual 
patterns that might indicate a cyber attack.
5. Cybersecurity automation: Machine learning algorithms can automate certain cybersecurity tasks, 
such as patching vulnerabilities or updating security protocols, which can help reduce the workload of 
security professionals.
Overall, the use of machine learning in cybersecurity has the potential to improve the effectiveness and efficiency of cyberdefense systems. However, it is important to carefully design and train machine learning algorithms to ensure that they do not introduce new vulnerabilities or compromise the security of systems.

Cybersecurity protects computers, servers, mobile devices, electronic systems, networks, and data from digital attacks, theft, and damage. It involves implementing technologies, processes, and policies to secure Systems and prevent unauthorized access to data.

There are many cybersecurity threats, including viruses, worms, Trojan horses, ransomware, phishing attacks, and denial of service attacks. Cybersecurity professionals work to identify and mitigate these threats by implementing measures such as firewalls, antivirus software, and intrusion detection systems.

In addition to protecting against cyber attacks, cybersecurity also involves protection against the unauthorize misuse of data. This includes implementing encryption, access controls, and secure data storage practices.

Overall, cybersecurity aims to ensure the confidentiality, integrity, and availability of data and systems in 
the face of ever-evolving digital threats.

## Problems we are going to coverd
1. Finding the malicious threat on the dataset
2. Clustering the malicious threats using Hierarchical Cluster 
3. Predicting the amount of bandwidth used by a network connection based on the amount of data transferred and the duration of the connection

### Finding the malicious threat on the dataset 
| Model Name   | Accuracy Score || Recall Score  | Excution Time |
| ------------- | ------------- || ------------- | ------------- |
| Decision Tree  | 0.99  || 0.99  | 15-30 Seconds  |
| SVM  | 0.98   || 0.96  | 19-21 Minutes  |

###  Clustering the malicious threats using Hierarchical Cluster
Similar items are grouped in hierarchical clustering, also known as hierarchical cluster analysis. The 
final product is a collection of clusters, each of which is unique from the others and whose members 
share several characteristics (Bock, 2019).
the most fundamental technique in Hierarchical Cluster
1. Agglomerative: Treat each data point as its Cluster at the outset; then, combine the Clusters that
are geographically closest to one another at each iteration. It's a bottom-up approach, to be sure. 
Initially, each dataset is treated as a separate unit. Clusters merge with other clusters at each 
iteration until a single cluster is produced

Model Evalution - 0.95

### Predicting the amount of bandwidth used by a network connection based on the amount of data transferred and the duration of the connection

By fitting a linear model to the data, one may predict how a continuous dependent variable will change in response to changes in one or more independent variables (Raschka, 2017).
There is two types of Linear Regression :
1. Simple Linear Regression: Modeling the association between a single feature (explanatory 
variable x) and a continuous-valued response (target variable y) is the purpose of simple 
(univariate) linear regression. (Raschka, 2017)
2. Multiple Linear Regression: In the preceding part, presented linear regression as a statistical 
method, and in this context, focused specifically on the instance when there was only one 
explanatory variable. Multiple linear regression allows us to expand the linear regression model 
to incorporate additional explanatory variables. (Raschka, 2017)
###What is the Bandwidth?
"Bandwidth" refers to the maximum rate at which information may be transferred through a network or 
the Internet. This metric measures how much data can be sent in each amount of time over a given
connection. Increases in network bandwidth allow for more excellent data transfer rates in both directions
(verma, 2022).
For Predict the Bandwidth using the Multiple Linear Regression. Therefore, chose those features for the model :
• The amount of data transferred: Total Forward Packets as a independent variable
• The duration of the connection – Flow Duration as an independent variable 
• ‘Flow Byts/s’ as a dependent variable. In CIC IDS 2018, there isn’t a feature that shows
bandwidth; one possibility is to use the "Flow Byts/s" feature, which is the number of bytes transferred per second for each network connection

## Ensemble Learning for Classification Models
The goal of ensemble methods is to combine different classifiers into a metaclassifier with better 
generalization performance than each classifier alone. (Raschka, 2017).
Using CIC-IDS 2018 dataset in Colab, getting high ram and crashing the terminal when executing two 
models in one notebook. In that case using same created models for ensemble learning.

## Conclusion 
Using CIC-IDS 2018 Dataset created three problems and made suitable models for each problem. For the first problem, There were created two models but suitable model in Decision Tree model. For the clusteringproblem (Problem 2) used the hierarchical clustering method because of CIC-IDS 2018 dataset is large dataset and it gives the identify clusters. Linear Regression models also show the good performance on the problem 3. After created the classification models for the problem 1, used the same Decision Tree model and SVM model for ensemble learning. It gives the good model performance that means these models can used it for finding threat on Network by pattern and finding the bandwidth of the network. 
