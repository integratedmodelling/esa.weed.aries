
The quality of the maps produced and the reference data (mainly points) used as reference may differ in different areas; for this reason, we want the Champion users to validate or point out the different issues in the current data (maps and points)
By the end of the project, we'll try to converge all tools and features in a single place, but for the time being there are still two main tools that cna be used for the assessment:
1. Assessment in the WEED application, used for visualisation of the final maps, but also of the input data and the documentation of the models. You can also download the data at the original resolution from here.
2. Assessment in the WEED RDM (Reference Data Module), used to obtain quantitative analysis and manage the reference points;

# Visual assessment
Report any errors or inconsistencies that should be improved, based on your knowledge of the area mapped.
This can include ecosystem delineation that looks coarse or blocky rather than natural and smooth (likely caused by coarse data used in ht eundelrying mdoel, whose effects are not smoothed out)

# Quantitative assessment
This analysis can leverage the confusion matrix, which can be triggered via the RDM.
TODO: explain how to interpret the confusion matrix

# Qualitative assessment of the data reference
The accuracy of the quantitative analysis may be impacted by incorrect reference data points:
1. wrong label (i.e.,  the location is dominated by a different Ecosystem Type, and the label should be corrected);
2. higher or lower uncertainty: you cna add a label High, Medium, Low for each point to identify the confidence of that reference point
3. generate your own reference point in the RDM
4. Add your own reference dataset in the RDM
Data > Upload New

<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/e5b816ef-96dc-43c8-8259-5ee9af0712f8" />



### Access the WEED application:

Please note: To trigger the  computation of an area that was not calculated yet, you'll need to use the WEED application

### Access the RDM:
**1. Go to: https://weed-rdm.iiasa.ac.at/**
<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/b2d7b719-e14d-4ada-b938-6e8dc3f1adb1" />

**2. Sign in using CDSE credentials**
<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/31eb657a-b2b2-4d37-ac21-955ae25c9448" />

**3. Open the Validation tab**
<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/66d81bb0-d7d2-4d48-89bf-7f78346a36fb" />

**4. Define the setting for your validation analysis:**

A. Draw a polygon or upload a geojSON to define the geographic area to analyse

B. Model approach: RuleBased or Machine Learning

C. Typology: IUCN GET (outside EU) or EUNIS (only for EU)

D. Validation Method: Onsite or Offsite

<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/23ca9960-9351-4815-aa1a-f2f76b33a47a" />

**5: Generate the confusion matrix**
<img width="960" height="516" alt="image" src="https://github.com/user-attachments/assets/ff671c72-b335-44f0-b37f-ec96f6f7db10" />

6. Accuracy calculation is triggered, and results become available in the Results tab

<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/d57a8c64-40e6-4ae4-ab39-caa7943004ce" />


<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/bb430948-65fb-4c35-af20-563fee4175f3" />

**7. Download the confusion matrix **
Results > Excel
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/21298cbc-ce9a-4e4e-80b4-f95eeb5cbba3" />
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/56a3f63a-8358-4662-a1d4-b919f71df954" />
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/f7db1990-ddf4-48d8-93fe-8d618183e6d5" />

8. Interpret the results from the validation


9. 




#### Validation Method

##### Onsite


##### Offsite
