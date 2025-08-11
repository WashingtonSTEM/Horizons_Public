# Washington STEM's Horizons Technical Assistance Templates
Today, only 40% of high school graduates in Washington enroll in higher education; however upwards of 80% of well-paying jobs in the state require some sort of postsecondary credential. This means many students, most often students of color and low-income students, will not have access to family-sustaining jobs and secure careers. 

Washington STEM manages the Horizons grants, a four year regional partnerships to boost student transitions from high school to 1-year certificate programs, two- and four-year degree programs and apprenticeships. The Horizons partnerships, funded by the Bill & Melinda Gates Foundation includes K-12 schools, colleges, and community-based organizations in the Olympic and Kitsap peninsulas, the Southwest region, the Palouse, and South King County.

Washington STEM also provides technical assistance to regional partners as they build capacity around accessing and leveraging data to improve student outcomes. Other technical advisors in the partnership include Sankofa, Scholar Fund, and College Access: Research in Action (CARA). These experts in their field will work with education partners to, respectively, enhance measurement and evaluation, equity and student voice (surveys), and advising, all through a continuous improvement model aimed at sustainability.
## Contact
### Washington STEM general inquiries: info@washingtonstem.org
### Data specific inquiries: impact@washingtonstem.org

## R Script
### Last updated 8/11/2025. Templates created by Rachel Tavolacci (rachel@washingtonstem.org) & Mikel Poppe (mikel@washingtonstem.org).
### Code of Conduct: 
These templates are designed to help researchers and educators improve equitable
postsecondary readiness by better understanding patterns between high school experiences and
postsecondary outcomes. This dashboard can help 
* Challenge Hunches
* Understand patterns across high school coursetaking, financial aid completion, and postsecondary enrollment, persistence, and completion

These resources should be used to analyze strengths and weaknesses of the school system, not individual students, families, communties, or staff. 

Washington STEM's Horizons Technical Assistance Templates © 2025 is
licensed under Attribution-NonCommercial 4.0 International. To view a copy of this license, visit
http://creativecommons.org/licenses/by-nc/4.0/
### Suggested Citation: 
Washington STEM. (July 2025). Horizons Technical Assistance Templates. Retrieved on XX/XX/XXXX from:
https://github.com/WashingtonSTEM/Horizons_Public

#### The script notes action items where relevant. At the start of the script, you will need to set the current year and base directory. 

### 1.Data Folder:
Contains subfolders of all raw and processed data needed to run scripts and connect to workbook. Mirror the folder structure in your directory in a parent folder named "Horizons" to easily run the script. The script notes download links for raw data.

### General overview: This template includes crosswalks specific to the Horizons Regional Partners. The script also excludes online schools. You may need to update crosswalks and excluded schools to fit your use case. *See Dataflow_Overview.xlsx for visual guide of script*
#### For any questions, please email impact@washingtonstem.org
1. Create the following folders in a local directory you would like to read and write data to. Add folders under Raw_Data and Cleaned_Data for additional years as relevant.
* Horizons/1.Data/Raw_Data/2025_Exports
* Horizons/1.Data/Cleaned_Data/2024
* Horizons/1.Data/Cleaned_Data/2025
* Horizons/1.Data/Dashboard_Files
  
2. These datasets contain prepped historical data, not available in this format in their raw, public form. Save them to your local folders.

    A) Found in the base of the Cleaned_Data folder of this repo -> save to to your local 'Horizons/1.Data/Cleaned_Data/' folder:
    * 2023_IPEDS_long.csv
    * FAFSA_10_Yr.csv
    * Sankey Template. xlsx
    * Regional_Analysis_Crosswalk.xlsx
  
    B) Found in 1.Data/Cleaned_Data/2024 of this repo -> save to your local 'Horizons/1.Data/Cleaned_Data/2024' folder:
    * RC_SQSS_Clean.csv
    * RC_Graduation_Clean.csv
    * Horizon_Graduates.csv

    C) Found in 1.Data/Raw_Data/2025_Exports of this repo -> save to your local 'Horizons/1.Data/Raw_Data/2025' folder
    * FAFSA Completion by Subgroup Report for Horizons Partnerships.xlsx
  
3. Download raw data for 2025 (& additional years as needed), as noted in the script. Save the raw data to *1.Data/Raw_Data/2025_Exports* (& additional years as needed).
   
4. Update the current year in the script. Update the base directory in the script to match yours. *If needing to run multiple years (2025, + 2026, etc) use the script to run one year at a time to properly build prior year data sets.*
   
5. Make needed updates to the script, noted throughout the script as "Action Items". Run start to finish. See console notes and *Review Step* at the end of the script for quality check. As needed, make changes and rerun script.
   ## Potential updates needed, noted as "Action items":
   * Review the *Check for changed column names and update as needed, then run remainder of script* ouptut and add code to need rename columns immeditaly after reading in new file to ensure script works properly.
   * Add new redacted ranges to the *#Function to clean any improper redacted ranges* as instructed by *⚠️ Values in RedactedPct containing letters (possible issues)* message in the console after running script.
   
6. Download the workbook (found in the workbook folder of this repo) and reconnect to the newly written files in your local *1.Data/Dashboard_Files* folder. Using the Missing_Districts.csv file, update data note text in workbook as needed. Save your own version of the workbook!


# Learn more:
To dive deeper into the student experiences and adult biases which impact postsecondary transitions, explore our H2P work: https://github.com/WashingtonSTEM/H2P_Public/
* Latest blog: https://washingtonstem.org/schools-are-reimaging-postsecondary-pathways/
* High School to Postsecondary collaborative toolkit (2024): https://washingtonstem.org/college-and-career-readiness-toolkit/
