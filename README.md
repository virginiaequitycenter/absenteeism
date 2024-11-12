# Exploring Chronic Absenteeism in Charlottesville & Albemarle 

Report: [Exploring Chronic Absenteeism in Charlottesville and Albemarle](https://virginiaequitycenter.github.io/absenteeism/absenteeism)

Last updated: 11/12/2024

This repo contains the code, data, and report for tracking and visualizing chronic absenteeism in Charlottesville City and Albemarle County public schools. 

The [Virginia Department of Education](https://www.doe.virginia.gov/programs-services/student-services/attendance-school-engagement) defines chronic absenteeism as

> *"missing ten percent or more of the academic year for any reason, including excused absences, unexcused absences, and suspensions."*

Based on a 180-day school year, that means approximately 18 days per year or 2 to 3 days per month.

## How to use this repo

**Step 1. Download the data**

The script `absenteeism.R` downloads the data directly from the VDOE website and prepares it for analysis. The raw data is saved in the `data/` folder and the cleaned data is saved as `chronic_absenteeism.csv`. 

As an extra layer of security, the VDOE website requires that only browsers download the data, rather than programatically with RStudio via an API call. This helps prevent DDOS attacks, or other instances of crawlers that might slow the website. 
To bypass this configuration, we have to manually supply some information to the API call so that it thinks RStudio is a browser. If you do not do this you'll get a **403: Forbidden** error, which means that the VDOE server understands the request but cannot fulfil it.  

**Step 2: Run the report**

The script `absenteeism.Rmd` creates the visualizations for Charlottesville and Albemarle. The report is then deployed via Github pages at https://virginiaequitycenter.github.io/absenteeism/absenteeism.

 
