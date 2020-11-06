# Track&Know Pilot 2 Synthetic Data Generator

## About Track & Know

<img src="https://github.com/ibadkureshi/tnk-locationallocation/blob/master/docs/images/proj-logo.png?raw=true" align="right" alt="Track&Know Logo" >

* **Project Title** - Big Data for Mobility Tracking Knowledge Extraction in Urban Areas
* **Project Website** - `https://trackandknowproject.eu/`
* **Work Package** - WP6: Pilots [*Leader: SIS*]
* **Task & Deliverable** - 6.3 Pilot 2: Healthcare service [*Leader: PAP*]
* **Component Leader** - Inlecom Group

## Acknowledgement

!["Funded by EU logo"](https://github.com/ibadkureshi/tnk-locationallocation/raw/master/docs/images/EU-H2020.jpg "Funded by EU H2020") This project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 780754.

## About

This notebook generates a synthetic dataset of patient appointments and referrals to a fictional service in the North East of England. The code can be adjusted to incorporate any area on mainland Great Britain. NI or the islands can be integrated too, however the structure of postcode, GP and OSA public data is different, and data input handlers will need to be adjusted.

The behaviour of the patients (visiting their nearby GP followed by attending a specialist clinic), appointments (clinic appointments within 7day-6weeks of the referral (gp appointment)), and facilities (one major facility taking the load, along with minor facilities) is meant to mirror the real data used under Pilot 2 of the Track & Know Project.

Real postcodes, from Royal Mail, are used to generate the appointment population, real facilities are used based on the British Lung Foundations study of Obstructive Sleep Apnea, and real GP's are used based on public data from the NHS. 

**All data is randomly generated and changes with every run of the generation code. Any resemblance to actual events or locales or persons, living or dead, is entirely coincidental.**

This data differs from the original data in that postcodes from the catchment are randomly selected. There were patterns in the occurrences of OSA and the referral schedules within the real data that are not reproduced in this synthetic dataset. These patterns are not reproduced because reapplication of this code (w/ the pattern reproduction) on the Track&Know pilot catchment area *could* lead to an exposure of actual patients.

Please read the 'Variable Operationalisation' document for more information about the output of this code.

Please refer to the Track&Know website for more information about the project and Pilot 2. https://trackandknowproject.eu

## The Data

The synthetic data can be found in the output folder. There are currently two files there.

* An appointment log that includes all the patient appointment information.
* A demand file which only includes latitude, longitude, and patient id.

Additionally, a file call VARIABLE-OPERATIONALISATION.txt is available that describes each column of data.

## The Generator

The included Python3 Jupyter Notebook includes the full methodology and code required to generate this dataset. The code can be adjusted to target a different part of the UK.

To use the generator public data is required. The sources of each piece of public data is available in the notebook. All data needs to be unzipped and placed in the input folder. This code does not redistribute the input data as we do not hold the copyright. Please refer to the README file in the input folder.
