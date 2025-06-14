# Measure Tables

## Measures Overview

The measure tables contain test results with values for all patients, split into physiological related areas for ease of use.  Checks should be undertaken to verify that the values are within expected clinical ranges. 

### Common Fields
Each table has the following fields:

| fieldname  | description                                                     |
| ---------- | --------------------------------------------------------------- |
| label      | descriptive label of the table contents. eg 'diabetes'          |
| area_id    | area id for GP Practice                                         |
| ods_code   | ODS (Organisation Data Service) identifier for the GP Practice. |
| person_id  | identifier of person                                            |
| patient_id | identifier of patient at a practice                             |

### Information format:

**`table name` (relationship)**
**Measure (full title and synoymns)**
*The business rules syntax used to create the table with (CLUSTER ID)s and date ranges.*    
Table of fieldnames + description specific to the table  
Additional information  

***
## `measures_blood` (Blood related)
Measurements of components or substances found within blood.

### HbA1c (Glycated Haemoglobin)
*HbA1c IFCC code (IFCCHBAM_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| hba1c_latest_date  | latest date of HbA1c IFCC code               |
| hba1c_latest_code  | SNOMED concept id for latest HbA1c IFCC code |
| hba1c_latest_name  | code term for latest HbA1c IFCC code         |
| hba1c_latest_value | value associated to latest HbA1c IFCC code   |

### Cholesterol (Total Serum)
*Total Cholesterol code (CHOL2_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| chol_latest_date  | latest date of Total Cholesterol code               |
| chol_latest_code  | SNOMED concept id for latest Total Cholesterol code |
| chol_latest_name  | code term for latest Total Cholesterol code         |
| chol_latest_value | value associated to latest Total Cholesterol code   |

### FBG (Fasting Plasma Glucose, FPG)
*Fasting Plasma Glucose code (FASPLASGLUC_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| fbg_latest_date  | latest date of Fast Blood Glucose code               |
| fbg_latest_code  | SNOMED concept id for latest Fast Blood Glucose code |
| fbg_latest_name  | code term for latest Fast Blood Glucose code         |
| fbg_latest_value | value associated to latest Fast Blood Glucose code   |

### eGFR (estimated Glomerular Filtration Rate)
*eGFR code (EGFR_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| egfr_latest_date  | latest date of eGFR code               |
| egfr_latest_code  | SNOMED concept id for latest eGFR code |
| egfr_latest_name  | code term for latest eGFR code         |
| egfr_latest_value | value associated to latest eGFR code   |

### Serum Creatinine
*Serum Creatine code (CRE_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| creat_latest_date  | latest date of Serum Creatine code               |
| creat_latest_code  | SNOMED concept id for latest Serum Creatine code |
| creat_latest_name  | code term for latest Serum Creatine code         |
| creat_latest_value | value associated to latest Serum Creatine code   |

### Liver Function Test
*Liver Function Test code (LFT_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| lft_latest_date  | latest date of Liver Function Test code               |
| lft_latest_code  | SNOMED concept id for latest Liver Function Test code |
| lft_latest_name  | code term for latest Liver Function Test code         |
| lft_latest_value | value associated to latest Liver Function Test code   |

> Note:
> Liver Function Test includes a range of tests assessing liver function.  This data shows the latest test recorded in the patient's record - other LFT tests may have been recorded on the same day.

## `measures_body` (Body related)
Measurements of the physical body.

### BMI (Body Mass Index)
*BMI Value code (BMIVAL_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| bmi_latest_date  | latest date of BMI code               |
| bmi_latest_code  | SNOMED concept id for latest BMI code |
| bmi_latest_name  | code term for latest BMI code         |
| bmi_latest_value | value associated to latest BMI code   |

## `measures_heart` (Heart related)
Measurements of heart function.

### Blood Pressure (BP)
*Systolic / Diastolic Blood Pressure code (BP_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| bp_latest_date  | latest date of Blood Pressure code               |
| bpsys_latest_code  | SNOMED concept id for latest Systolic Blood Pressure code |
| bpsys_latest_name  | code term for latest Systolic Blood Pressure code         |
| bpsys_latest_value | value associated to latest Systolic Blood Pressure code   |
| bpdia_latest_code  | SNOMED concept id for latest Diastolic Blood Pressure code |
| bpdia_latest_name  | code term for latest Diastolic Blood Pressure code         |
| bpdia_latest_value | value associated to latest Diastolic Blood Pressure code   |
| bpparent_latest_code  | SNOMED concept id for latest parent Blood Pressure code |
| bpparent_latest_name  | code term for latest parent Blood Pressure code         |
| match_algorithm | number code of the algorithm used for Blood Pressure match   |

> Note:  
> **Parent Blood Pressure**  
> SNOMED code indicating a Blood Pressure activity, to which a Systolic and Diastolic code pair are linked.
>
> **Match Algorithm**  
> 1. Systolic matched to diastolic using their common parent  
> 2. Systolic matched to diastolic with nearest record id  
> 3. Systolic matched to only diastolic recorded on the same date  
> 4. Systolic matched to diastolic based ranked date and record id  
> 
> For full information see [Analysis: Blood Pressure](../Analysis/Blood_Pressure.md)
### Pulse Rate 
*Pulse Rate code (PLSRATE_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| pulserate_latest_date  | latest date of Pulse Rate code               |
| pulserate_latest_code  | SNOMED concept id for latest Pulse Rate code |
| pulserate_latest_name  | code term for latest Pulse Rate code         |
| pulserate_latest_value | value associated to latest Pulse Rate code   |

## `measures_lung` (Lung related)
Measurements of lung function.

### FEV1/FVC Ratio
*FEV1/FVC Ratio code (FEV1FVC_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| fev1fvc_latest_date  | latest date of FEV1/FVC Ratio code               |
| fev1fvc_latest_code  | SNOMED concept id for latest FEV1/FVC Ratio code |
| fev1fvc_latest_name  | code term for latest FEV1/FVC Ratio code         |
| fev1fvc_latest_value | value associated to latest FEV1/FVC Ratio code   |

### MRC Breathlessness Score
*MRC Breathlessness Score code (MRC_COD)*

| fieldname          | description                                  |
| ------------------ | -------------------------------------------- |
| mrc_latest_date  | latest date of MRC code               |
| mrc_latest_code  | SNOMED concept id for latest MRC code |
| mrc_latest_name  | code term for latest MRC code         |
| mrc_latest_value | value associated to latest MRC code   |

## `measures_risk` (Risk related)
Scores and indicators relating to clinical risk

### CHADSVASC (CHA~2~DS~2~VASc)
Risk of Stroke in patients with non-rheumatic Atrial Fibrillation
*CHADSVASC code (CHADVASC_COD)*



| fieldname              | description                                   |
| ---------------------- | --------------------------------------------- |
| chadsvasc_latest_date  | latest date of CHA2DS2VASC code               |
| chadsvasc_latest_code  | SNOMED concept id for latest CHA2DS2VASC code |
| chadsvasc_latest_name  | code term for latest CHA2DS2VASC code         |
| chadsvasc_latest_value | value associated to latest CHA2DS2VASC code   |

### QRISK
Risk of a CVD event within next 10 years
*QRISK code (QRISK2AND3SCORE_COD)*

| fieldname          | description                             |
| ------------------ | --------------------------------------- |
| qrisk_latest_date  | latest date of QRISK code               |
| qrisk_latest_code  | SNOMED concept id for latest QRISK code |
| qrisk_latest_name  | code term for latest QRISK code         |
| qrisk_latest_value | value associated to latest QRISK code   |

### Clinical Frailty Score
Assessment of overall fitness / frailty
*Clinical Frailty Score code (CLINFRAILSCR_COD)*

| fieldname                | description                                              |
| ------------------------ | -------------------------------------------------------- |
| frailty_cfs_latest_date  | latest date of Clinical Frailty Score code               |
| frailty_cfs_latest_code  | SNOMED concept id for latest Clinical Frailty Score code |
| frailty_cfs_latest_name  | code term for latest Clinical Frailty Score code         |
| frailty_cfs_latest_value | value associated to latest Clinical Frailty Score code   |

### Electronic Frailty Index
Risk stratification of frailty calculated from patient record
*Electronic Frailty Index code (FRAILEFI_CEG)

| fieldname                | description                                                |
| ------------------------ | ---------------------------------------------------------- |
| frailty_efi_latest_date  | latest date of Electronic Frailty Index code               |
| frailty_efi_latest_code  | SNOMED concept id for latest Electronic Frailty Index code |
| frailty_efi_latest_name  | code term for latest Electronic Frailty Index code         |
| frailty_efi_latest_value | value associated to latest Electronic Frailty Index code   |

### Frailty Status
*Frailty Status code (MILDFRAIL_COD, MODFRAIL_COD, SEVFRAIL_COD)*

| fieldname                   | description                                                         |
| --------------------------- | ------------------------------------------------------------------- |
| frailty_status_latest_date  | latest date of Frailty Status code                                  |
| frailty_status_latest_code  | SNOMED concept id for latest Frailty Status code                    |
| frailty_status_latest_name  | code term for latest Frailty Status code                            |
| frailty_status_latest_value | value associated to latest Frailty Status code                      |
| frailty_status              | Rockwood Frailty Scale term derived from frailty_status_latest_name |

> Note:
> The `frailty_status` column simplifies the code term provided by the `fraility_status_latest_name` to provide a consistent Rockwood Frailty Scale term: