# Column Names and Descriptions for Heart Attack Analysis Dataset
* `age`: age of the patient
* `sex`: sex of the patient
    - 0 = male
    - 1 = female
* `cp`: Chest Pain type
    - 0 = typical angina
    - 1 = atypical angina
    - 2 = non-anginal pain
    - 3 = asymptomatic
* `trtbps`: resting blood pressure (in mm Hg)
* `chol`: cholestoral in mg/dl fetched via BMI sensor
* `fbs`: (fasting blood sugar > 120 mg/dl)
    - 0 = false
    - 1 = true
* `restecg`: resting electrocardiographic results
    - 0 = normal
    - 1 = having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV)
    - 2 = showing probable or definite left ventricular hypertrophy by Estes' criteria
* `thalach`: maximum heart rate achieved
* `exng`: exercied induced angina
    - 0 = no
    - 1 = yes
* `oldpeak`: ST depression induced by exercise relative to rest
* `slp`: the slope of the peak exercise ST segment
    - 0 = unsloping
    - 1 = flat
    - 2 = downsloping
* `caa`: number of major vessels (0-3)
* `thall`: thalessemia
    - 0 = null
    - 1 = fixed defect
    - 2 = normal
    - 3 = reversable defect
* `output`: diagnosis of heart disease (angiographic disease status)
    - 0: < 50% diameter narrowing. less chance of heart disease
    - 1: > 50% diameter narrowing. more chance of heart disease

### Medical Definitions
<b>Angina</b>: chest pain due to reduced blood flow to the heart muscles. There're 3 types of angina: stable angina, unstable angina, and variant angina. To know more about angina click here: https://www.nhs.uk/conditions/angina/#:~:text=Angina%20is%20chest%20pain%20caused,of%20these%20more%20serious%20problems.

<b>Cholesterol</b>: a waxy substance found in the body cells and it belongs to a group of organic molecules called lipids. There are 3 types of cholesterol; high-density lipoprotein (HDL) and it's known as the "good cholesterol", low-density lipoprotein (LDL) known as the "bad cholesterol", and very-low-density lipoproteins (VLDL) and as the name implies, they're low dense particles that carry triglycerides in the blood.

<b>ECG</b>: short for electrocardiogram, it's a routine test usually done to check the heart's electrical activity.

<b>ST depression</b>: a type of ST-segment abnormality. the ST segment is the flat, isoelectric part of the ECG and it represents the interval between ventricular depolarization and repolarization. For more details check this link: https://litfl.com/st-segment-ecg-library/.

<b>Thalassemia</b>: it's a genetic blood disorder that is characterized by a lower rate of hemoglobin than normal.