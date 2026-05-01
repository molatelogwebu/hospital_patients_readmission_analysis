Hospital Readmission Analysis

Analysing hospital readmission trends using Excel.

Project Overview
This project analyzes hospital readmission data to identify patterns and factors contributing to patient readmissions.

Dataset

The dataset is stored in the hospital readmission analysis folder and contains patient level hospital data including:
- Admission details
- Diagnosis information
- Readmission status
- Patient id
- Admission Date
- Season
- Age
- Gender
- Region
- Primary diagnosis
- Comorbidities Count
- Length of Stay
- Treatment type
- Medications count
- Followup Visits Last Year
- PreviousReadmissions
- Insurance Type
- Discharge Disposition
- Readmission Risk Score
- Label
- Age Group
- Admission Month
- Admission Year
- Readmission Risk Category
- Frequent Patient Flag

Objectives

- Identify key factors influencing readmissions
- Analyze trends across patient groups
- Support healthcare decision-making

Tools Used
- Excel
- Power Bi

- Data Cleaning:  
1. Checked for duplicates — none found.
2. Handled missing values:
a.  Text Columns:
=IF(C2="";”UNKNOWN”C2)
b. Numeric Columns:
=IF(B2="";0; H2)
c. Standardized text columns using:
=PROPER(TRIM(F2))
=UPPER(TRIM(E2))
d.  Validate Age:
=IF(OR(D2<0;D2>120),”CHECK”D2)

Calculations;
1. Age Group
=IF(D2<18;”Child”;IF(D2<40;”Young Adult; IF(D2<65;”Adult”, “Senior”)))
2. Admission Month
= TEXT(B2;”MMM”)
3. Admission Year
= YEAR(B2)
4. Readmission Risk Category
=IF(P2<0.3,"Low",
IF(P2<0.7,"Medium","High"))
5. Frequent Patient Flag
=IF(M2>=3,"Frequent","Normal")

Link to PowerBI; 
https://app.powerbi.com/groups/me/reports/5c89e5c2-dfc5-411c-9819-b371667ee48a/669cb6ba0ac9040b050d?experience=power-bi

Dataset source:
Kaggle.com 

Author
- Molatelo Gwebu
