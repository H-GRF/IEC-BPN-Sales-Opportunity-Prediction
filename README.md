
# IEC-BPN Sales Opportunity Prediction

## BNP PARIBAS: Predicting Cross-Selling Opportunities for a Bank

### IEC-BPN Sales Opportunity Prediction


## Overview

### Start
- May 9, 2024

### Close
- May 11, 2024


## Description

Welcome to the IEC Algeria Data Cup "Bank Sales Opportunity Prediction," an exciting machine learning competition organized by the student club "IEC" to showcase their skills in data science and machine learning.

### Objective

In the banking sector, the ability to identify customers potentially interested in acquiring new products is crucial for optimizing cross-selling opportunities and improving customer satisfaction. This competition focuses on predicting which customers might be interested in acquiring additional products, such as a Visa Card, product insurance, or home insurance, based on detailed customer data, including age, gender, marital status, transaction history, and current products. Participants are encouraged to develop multi-label classification models to identify these cross-selling opportunities, helping the bank optimize its sales strategies and enhance customer experience.

### Evaluation

An appropriate evaluation metric for this type of multi-label classification task is the F1-micro score. The F1-micro score calculates the weighted average of the F1 scores for each class (in this case, each product) using the total number of true positives, false positives, and false negatives. This provides an overall measure of the model's precision and recall across all product classes.

The formula for the F1-micro score is:

\[ \text{F1}_{\text{micro}} = \frac{2 \times (\text{precision} \times \text{recall})}{\text{precision} + \text{recall}} \]

where:
- Precision is the number of true positives divided by the number of true positives plus false positives.
- Recall is the number of true positives divided by the total number of true positives and false negatives.

The F1-micro score is a useful metric for evaluating the overall performance of the model across all product classes, considering both precision and recall.

## Submission File

The first line of the file contains the column names - "id_client" and a set of products. Each subsequent line corresponds to a set of predictions (probabilities from 0 to 1) for a particular combination of client and products.

You can refer to the `SampleSubmission.csv` file in the data section.

```
id_client  CARTE_VISA  DÉCO  MRH  PACK_BLEDI_ARE  TOUT_EN_UN  COMPTE_D_EPARGNE_ZÉRO  COMPTE_DÉVISE
9352       0           0     1    1               0           0                       1
6969       1           0     0    0               0           1                       0
9696       1           0     0    0               0           0                       1
```

## Citation

ADC IEC (2024). Sales Opportunity Prediction. Kaggle.  
[https://www.kaggle.com/competitions/iec-bnp-prediction-des-opportunites-de-vente](https://www.kaggle.com/competitions/iec-bnp-prediction-des-opportunites-de-vente)

## Dataset Description

The dataset consists of approximately 76,000 clients.

### Files

- `train.csv` - the training set
- `test.csv` - the test set
- `sample_submission.csv` - a sample submission file in the correct format

### Data fields

- `id_client` : Client identifier
- `Nom de l'agence` : Name of the agency
- `Catégorie de clientèle` : Client category (500: Individuals, 550: Professionals privately, 555: Algerians living abroad)
- `Age` : Client age
- `Genre` : Client gender (1: Male, 2: Female)
- `Etat civil` : Marital status (0: Not specified, 1: Single, 2: Married, 3: Widowed, 4: Separated, 5: Divorced, 6: Partnered, 8: Not applicable, 9: Unknown)
- `Pays_naissance` : Country of birth (pseudonymized for privacy)
- `Code_pays_nationalité` : Nationality code (pseudonymized for privacy)
- `Statut de résidence fiscale` : Tax residency status (1: Resident, 2: Non-resident)
- `Activité Principale Economique` : Primary economic activity (e.g., 41: Construction, 01: Fisheries)
- `Catégorie socio-professionnelle` : Socio-professional category (e.g., Lawyer, Notary, Doctor)
- `nom_employeur_1` : Employer name (pseudonymized for privacy)
- `Secteur Activité Economique Local` : Local economic activity sector
- `Démarches Collectives` : Collective actions taken by the client
- `Notation` : Credit rating of the client
- `Segment commercial` : Commercial segment classification
- `Ancienneté` : Client tenure with the bank

### Financial Data

- `Moyenne des mouvements créateurs réels` : Average of real incoming transactions
- `Moyenne des mouvements créateurs fictifs` : Average of fictitious incoming transactions
- `Moyenne des mouvements destructeurs réels` : Average of real outgoing transactions
- `Moyenne des mouvements destructeurs fictifs` : Average of fictitious outgoing transactions
- `Moyenne de solde maximal mensuel` : Average maximum monthly balance
- `Moyenne de solde minimal mensuel` : Average minimum monthly balance
- `Moyenne de solde de fin du mois` : Average end-of-month balance
- `Moyenne de solde moyen mensuel` : Average monthly balance
- `Médiane des mouvements créateurs réels` : Median of real incoming transactions
- `Médiane des mouvements créateurs fictifs` : Median of fictitious incoming transactions
- `Médiane des mouvements destructeurs réels` : Median of real outgoing transactions
- `Médiane des mouvements destructeurs fictifs` : Median of fictitious outgoing transactions
- `Médiane de solde maximal mensuel` : Median maximum monthly balance
- `Médiane de solde minimal mensuel` : Median minimum monthly balance
- `Médiane de solde de fin du mois` : Median end-of-month balance
- `Médiane de solde moyen mensuel` : Median monthly balance

### Products (Targets)

- `Carte Visa` : A Visa card
- `DECO` : Insurance products (Accident or general health insurance)
- `MRH` : Home insurance
- `PACK BLEDI` : A product pack for Algerians living abroad
- `TOUT_EN_UN` : One of three bundled products: TOUT EN UN DECOUVERTE, TOUT EN UN REFERENCE, TOUT EN UN SERENITE
- `Compte d'épargne à taux zéro` : A zero-interest savings account
- `COMPTE DÉVISES` : A foreign currency account for daily financial operations
