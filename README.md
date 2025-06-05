# UEFA Չեմպիոնների Լիգայի Հաղթողի Կանխատեսում

Այս նախագիծը իրականացնում է UEFA Չեմպիոնների Լիգայի (UCL) 2024 թվականի հնարավոր հաղթողի կանխատեսում՝ օգտագործելով պատմական տվյալների վրա ուսուցանված մեքենայական ուսուցման մոդել։ Տվյալները վերլուծվում են PCA-ով (Գլխավոր բաղադրիչների վերլուծություն) և կիրառվում է լոգիստիկ ռեգրեսիա։

## Օգտագործված տվյալներ
 
- ucl_stats.csv — Պարունակում է թիմերի 1993-2020թթ-երի վիճակագրական տվյալներ՝ հաղթանակներ, պարտություններ, խփած և բաց թողած գոլեր և այլն։

- AllTimeRankingByClub.csv — Պարունակում է պատմական վարկանիշային տվյալներ։

## Օգտագործվող գրադարաններ

- import pandas as pd
- import numpy as np
- import matplotlib.pyplot as plt
- import seaborn as sns
- from sklearn.model_selection import train_test_split
- from sklearn.preprocessing import StandardScaler
- from sklearn.decomposition import PCA
- from sklearn.linear_model import LogisticRegression
- from sklearn.metrics import classification_report, confusion_matrix, ConfusionMatrixDisplay

 ### Նկարագրություն
 
Նախագիծը բաղկացած է հետևյալ հիմնական փուլերից․

### Տվյալների ներմուծում

- ucl_stats.csv

- AllTimeRankingByClub.csv

### Նախնական մշակում

- Կատեգորիական տվյալների վերափոխում (Club, league)։

- Նոր հատկանիշների հաշվարկ (հաղթանակների տոկոս, գոլերի հարաբերակցություններ և այլն)։

### Տվյալների նորմավորում և PCA

- Նորմավորում՝ StandardScaler։

- Հիմնական բաղադրիչների անալիզ (PCA)՝ չափերը փոքրացնելու համար։

### Մոդելի ուսուցում

- Լոգիստիկ ռեգրեսիա (LogisticRegression)։

- Կարգավորում անհավասար դասերի դեպքում՝ class_weight='balanced'։

### Կանխատեսում և գնահատում

- Քննարկում ենք մոդելի արդյունքները՝ classification_report, Confusion matrix։

- Թիմերի հավանականությունների վիզուալիզացիա։

### Վերջնական կանխատեսում

- Մոդելը ընտրում է առավել հավանական հաղթողին՝ ըստ ամենաբարձր հավանականության:


