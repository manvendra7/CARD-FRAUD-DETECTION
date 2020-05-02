# IEE CIS CARD FRAUD DETECTION 

[DETAILED REPORT](https://docs.google.com/document/u/1/d/e/2PACX-1vTaHuO1OausEJli70VwXYJQzkVJPbm3mRLqZTUN1Ks-aepcGinko8hcmVCAfXEn1g/pub)


## Introduction
Suppose it is Christmas time and you are throwing a party at your house. You have called all
your friends and family. So you go to the supermarket to do some shopping. Standing at the cash
counter with a long line behind you the cashier tells you that your card has been declined. With
bags full of gifts, wines and cakes you try one more time. But, still the cashier announces that
your card has been declined and after sometimes you receive a message ‘Press 1 if you just tried
to do transaction of 15000 at Chris supermarket. So, what’s just happened with you is the
companies fraud detection system of the card you are using finding some unusual patterns in
your transaction.
Card fraud is a term used for theft and fraud committed using a payment card, such as debit or
credit card as a fraudulent source of funds in the transaction. It can be done either by theft of
actual card or by illegally obtaining the cardholder’s account and personal information.
Technologies have existed since the early 1990s to detect potential fraud. With the help of
machine learning we can find the pattern of usual and unusual behavior of client’s transaction in
order to block likely frauds.

## PROBLEM DEFINITION:
1. If some kind of fraud happens the card should be blocked immediately.
2. Model should avoid predicting a legitimate transaction as fraudulent.

## MOTIVATION:
Card fraud costs consumers and financial company millions of dollars annually. While the
fraudsters continues to come up with new ideas and tricks. Fraud prevention system is saving
millions of dollars per year. We want to improve this figure using machine learning algorithms
with great user experience.

## CONCEPTUAL IDEA:
Through machine learning algorithms, millions of transactions can be searched to spot patterns
and detect fraudulent transactions. For example consider
* Scenario 1: Irregularity in the transaction pattern

  A person does a transaction of 10,000 on 1 st of every month from his debit card for a
  product named C, from his phone on a website named Z. This is his regular pattern of
  transaction. Now suppose one day there is a payment of 15,000 from his debit card for
  product named W from a different website.

  Possibility: There is a higher probability that the transaction can be fraudulent, but there
  is also a probability that the person himself is using his card for that product. As the
  product W was better and he wanted to try it.

* Scenario 2 : Higher probability of fraud cases from a location

* Scenario 3: Higher cases of fraud from a particular website

## DATA SOURCE:
The data is taken from IEEE, CIS fraud detection competition on kaggle. The data comes from
Vesta's real world e-commerce transactions and contains a wide range of features from client
identity, card details to transaction details.

**INPUT DATA:**

The data is broken in two data points’ identity and transaction which are joined by TransactionID. 

 **Identity Table: (Information about cards and client details)**

Identity Table has 144233 rows and 41 columns.
  
 Variables in this table are identity information – network connection information (IP, ISP, Proxy, etc.) and digital signature  (UA/browser/so/version, etc.) associated with transactions.
 
   **Features:**
   
      - DeviceType
      - DeviceInfo
      - Id12-id38
      - TransactionID etc.
  
 **Transaction Table: (Information about the transaction of the clients)**
 
  “It contains money transfer and also other gifting goods and service, like you booked a ticket for others, etc.” 
  Transaction table has 590540 rows and 394 columns.
  
  **Features:**
  
    - ProductCD
    - isFraud
    - Card1 – card6
    - TransactionID
    - addr1,addr2
    - P_emaildomain
    - R_emaildomain
    
    
  We will have a look at each variable in identity and transaction tables when we will do EDA.
  
  We have to merge the identity and transaction data points for our training data.
  
  Our Training dataset has total of 590540 instances and 434 variables. 
  
  **Output Data:**
  In the dataset the target variable is a binary attribute ‘isFraud’ ‘0’ or ‘1’ (“Yes” or “NO”). We have to predict the probability that the online transaction is fraudulent. 
  
  **Connection between Input and Output:**
  
  As per our dataset we need to deal with binary classification problem in order to achieve our goal. We are predicting the transaction as fraudulent or not i.e. as “1” (‘Fraud’) or “0” (Not Fraud). 

