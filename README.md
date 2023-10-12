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

## Features and Categories

The dataset comprises several features, each with a distinct set of categories. Here's an overview of the features and the number of categories within each:

1. **Gender**
   - Number of Categories: 2
   - Categories: 'Male' and 'Female'

2. **No-show**
   - Number of Categories: 2
   - Categories: 'No' and 'Yes'

3. **Employment**
   - Number of Categories: 3
   - Categories: 'Non Employed', 'Salaried', and 'Business'

4. **Location and Clinic Location**
   - Number of Categories: 5
   - Categories: 'Bengaluru', 'Chennai', 'Pune', 'Noida', and 'Coimbatore'

5. **Scheduled Day and Appointment Day**
   - Number of Categories: 7
   - Categories: 'Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', and 'Saturday'

6. **Appointment Type**
   - Number of Categories: 2
   - Categories: 'New Patient' and 'Follow-up Patient'

7. **Channel**
   - Number of Categories: 2
   - Categories: 'Call' and 'Web Portal'

This information provides a clear understanding of the features and the variety of categories present within each, which is valuable for data analysis and modeling.
