# No-Show-Based Patient Appointment System

The No-Show-Based Patient Appointment System is a data-driven solution designed to tackle the issue of patient no-shows in healthcare facilities. This project leverages data analysis, predictive modeling, and user-friendly applications to help healthcare providers reduce appointment no-show rates and improve patient care.

## Data Description

The dataset used in this project consists of 51,173 rows and 18 columns, providing insights into patient appointments and various associated factors. Here are detailed descriptions of the dataset columns:

- `Patient_ID`: A unique six-digit numeric identifier for each patient.
- `Gender (New)`: Gender information, categorized as 'M' for Male and 'F' for Female.
- `Gender`: Gender information, categorized as 'M' for Male and 'F' for Female.
- `Scheduled_Date`: The date when the appointment was scheduled.
- `Appointment_Date`: The date of the actual appointment.
- `Appointment_Time`: The time of the appointment.
- `Age (New)`: The age of the patient.
- `Age`: The age of the patient.
- `Hypertension`: Indicates whether the patient has hypertension, with values '1.0' for True and '0.0' for False.
- `Diabetes`: Indicates whether the patient has diabetes, with values '1.0' for True and '0.0' for False.
- `Alcoholism`: Indicates whether the patient is alcoholic, categorized as 'True' or 'False.'
- `Handcap`: Indicates whether the patient is a handicap, categorized as 'True' or 'False.'
- `No-show`: Indicates whether the patient will show for the appointment, with values 'Yes' or 'No.'
- `Employment`: The patient's employment status, with options including 'Business,' 'Non-Employed,' and 'Salaried.'
- `Doctor_Id`: A unique six-digit numeric identifier for the doctor.
- `Channel`: The method of booking the appointment, with options 'Call' or 'Web Portal.'
- `Rate_Of_Cancellation`: The cancellation rate after booking.
- `Day_Difference`: The difference in days between the appointment day and the scheduled day.


### Data Summary

- **Data Types**: The dataset comprises a mix of data types, providing a rich source of information for analysis:
  - Numeric Data: Numeric data types are present in columns such as `Age`, which represents the patient's age, and `Day_Difference`, indicating the difference in days between the appointment and scheduled day.
  - Categorical Data: Categorical data types are found in columns like `Gender`, `Clinic_Location`, `Location`, `Employment`, and `Channel`, providing information about gender, appointment locations, patient residences, employment status, and booking channels.
  - Boolean Data: Boolean data types are utilized in columns such as `Hipertension`, `Diabetes`, `Alcoholism`, and `Handcap` to indicate the presence or absence of specific conditions or characteristics.


### Sample Data

Here is a sample of the first few rows from the dataset to provide you with a glimpse of its content:

| Patient_ID | Gender (New) | Gender | Scheduled_Date | Appointment_Date | Appointment_Time | Age (New) | Age | Hypertension | Diabetes | ... | Clinic_Location | Doctor_ID | Scheduled_Day | Appointment_Day | Appointment_Type | Channel | Cancelled | Rate_Of_Cancellation | Day_Difference | Appointment_Hour |
|------------|--------------|--------|----------------|------------------|-----------------|-----------|-----|--------------|----------|-----|-----------------|-----------|--------------|----------------|-----------------|---------|-----------|----------------------|----------------|-----------------|
| 299000     | F            | F      | 29-04-2016     | 29-04-2016       | 22.05.00        | 26        | 62  | 1.0          | 0.0      | ... | Noida           | 4000.0    | Friday       | Friday         | Follow-up Visit  | Call    | 1.0       | 0.666667             | 0 days         | 22.0            |
| 5590000    | M            | M      | 29-04-2016     | 29-04-2016       | 21.32.00        | 52        | 56  | 0.0          | 0.0      | ... | Pune            | 1000.0    | Friday       | Friday         | New Patient      | Web Portal | 1.0       | 0.555556             | 0 days         | 21.0            |
| 42600      | M            | F      | 29-04-2016     | 29-04-2016       | 21.46.00        | 12        | 62  | 0.0          | 0.0      | ... | Coimbatore      | 1000.0    | Friday       | Friday         | New Patient      | Call       | 0.0       | 0.545455             | 0 days         | 21.0            |
| 8680       | F            | F      | 29-04-2016     | 29-04-2016       | 18.08.00        | 22        | 8   | 0.0          | 0.0      | ... | Pune            | 2000.0    | Friday       | Friday         | Follow-up Visit  | Web Portal | 0.0       | 0.589744             | 0 days         | 18.0            |
| 88400      | F            | F      | 29-04-2016     | 29-04-2016       | 20.22.00        | 26        | 56  | 1.0          | 1.0      | ... | Pune            | 3000.0    | Friday       | Friday         | New Patient      | Mobile Application | 1.0 | 0.535714             | 0 days         | 20.0            |


### Data Pre-processing

--> Some columns had null values :   To address the issue, those null values were removed.

--> To satisfy some specific datatype requirements, few columns datatype was changed.

--> To avoid confusion, some column names were standardized.

--> Various columns had categorical data . To convert categorical data into  numerical format  ‘Label Encoding’ was done.


### Exploratory Data Analysis

Here are some EDA analysis plots:

![image](https://github.com/suryaaaprakash/no_show_appointment/assets/147717009/3a16b142-3461-4ab2-90e2-d1496e328e5d)

![image](https://github.com/suryaaaprakash/no_show_appointment/assets/147717009/cd586f8b-5b8b-4a99-b16a-fb449c10c116)

![image](https://github.com/suryaaaprakash/no_show_appointment/assets/147717009/dc5eabb5-d0d9-4a5b-a8c6-b33d36004379)

![image](https://github.com/suryaaaprakash/no_show_appointment/assets/147717009/6fe51670-9f60-480d-96ec-d20383cfa66c)


### Feature Selection

For selecting the appropriate features for training the model , we check multicollinearity VIF and plot the correlation matrix.

### Models used

Logistic Regression

Naïve Bayes

Random Forest

Support Vector Machine

Ada boost Classifier

Gradient Boosting

XG Boost Classifier


### Model Building

When the models were trained on the dataset,

* The predictions were 0 biased due to class imbalance.

       So to address the class imbalance, SMOTE was used.
    SMOTE:  (Synthetic Minority OverSampling Technique)
  
    SMOTE is a resampling technique specifically designed to mitigate class imbalance by oversampling the minority class.

* After balancing the classes using SMOTE, the predictions were still 0 biased.

       So, the true positive  and true negative predictions were taken separately and trained on the models.
  This method also did not provide good results and yielded wrong predictions.

CLASS IMBALANCE- 0 AND 1 EQUAL:

- Checked the occurrences of each class.
  
- Found the minimum count between the two classes.
  
- Created a new DataFrame with the sampled data – ‘balanced_df’.

  'Balanced_df' contains an equal number of samples for both classes

![image](https://github.com/suryaaaprakash/no_show_appointment/assets/147717009/4c993fa4-1157-44b1-9a62-a3826e95af9f)

This dataset was used for model training and gave good results.












