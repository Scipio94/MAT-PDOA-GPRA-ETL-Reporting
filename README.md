# Peer Recovery Program Overview
The Peer Recovery Program (PRP) provides recovery support services for all patients who present with substance use disorder, to include opioid use disorder, in our emergency departments and on our inpatient floors. The program serves participating RWJBarnabas Health hospitals, 24 hours a day, 7 days per week through full-time, hospital-based recovery specialists. Funding is provided by the New Jersey Department of Health, Division of Mental Health and Addiction Services. The Peer Recovery Program is an initiative of the Tackling Addiction Task Force. The Peer Recovery Program is funded by the New Jersey Department of Human Services, Division of Mental Health and Addiction Services.

# Project Summary
To gauge the efficacy of the Institute for Prevention and Recovery's PRP program, the data collected from RWJBaranabas Health's hospitals-based recovery specialists will be coded and submitted in a format supplied via the Government Performance and Supplies Act (GPRA).

# Methods
To complete the project I utilized the python coding language using a variety of data manipulation methods and functions, creating six (6) distinct dataframes and joining them on a the unique identifier, 'ClientID', shared across all six (6) dataframes to create a complete file for submission. Additionally, there was some data clean up and manipulation done in excel as well done to refine the final file further.

# Data Preparation
Create a copy of the following column prior to coding:
- SPEAK_LANGUAGE_OTHER_THAN_ENGLISH
  - Column should be named: SPEAK_LANGUAGE_OTHER_THAN_SPANISH
  - If SPEAK_LANGUAGE_OTHER_THAN_ENGLISH = ‘No’ then SPEAK_LANGUAGE_OTHER_THAN_SPANISH = ‘Yes’
  - If SPEAK_LANGUAGE_OTHER_THAN_ENGLISH = ‘Yes’ then SPEAK_LANGUAGE_OTHER_THAN_SPANISH = ‘No’
 
When running MAT-PDOA GPRA 4 use the **df['MEDICATION_PLANNED'].unique()** script to ensure that the MEDICATION_PLANNED column is empty
 
# Data Cleaning MAT-PDOA
Implement QA on the following columns:
- BatchID column can be left blank
- QAOnly  column can also be left blank
- There should be two SvcOtherMedical columns
  - Will have to delete variables x and y
- GrantNo : TI085280
- Omit the following columns for Intakes and after omitting the irrelevant columns, PATIENT, MRN, etc.:
  - ST:ABJ2:ABJ[LAST ROW] – CLEAR Contents
  - Column ON – SvcOtherMedical
- Omit the following columns for Follow-Ups and after omitting the irrelevant columns, PATIENT, MRN, etc:
  - O2:BQ[LAST ROW]
  - LZ2:PO[LAST ROW]
  - SX2:ABK[LAST ROW]
- If FLWPStatus blank insert value 32 and input ‘None’ in SPEC column
- Check MHDiagnosis columns 
- Check OverdoseInter Columns
- Check OverdoseInter columns, if Overdose = 1 and all 0s, then all should be -9



