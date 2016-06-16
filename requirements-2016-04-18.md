# Requirements for ANDI web application

## Input page

### 1. Normative Data

Should not be a drop down menu. Instead it is preselected on the latest version with a small button for ‘older version’ next to it. This will give a pop up in which an older version can be selected.  I would rename this  `Database version`.

~~### 2. Search for relevant tests~~

~~Should be `Search for neuropsychological tests`.~~

### 3. Tests in tree structure

Should be searchable both by test category (as it is now) as well as by the alphabet.

### 4. Selected tests

Should be removable by a clickable ‘x’ next to the name.
When you remove test in first tab it should be reflected in second tab.
When you remove test in second tab it should be reflected in first tab.

### 5. Selected tests

Should display the entire test + variable name (Long name 1 + Long name 2 + (if needed) Long name 3) from the template.

### 43. The 'download template' button should only appear after clinicians have selected some tests. Else its just downloading an empty template which I think will be confusing.

### 6. Selected tests

Should be drag-able to a preferred order by clinicians.

When clinician selects a test it shows up in the list on the right. From there clinicians should be a. Able to rempve them by clicking a cross and b. Vertically be able to drag and drop in the order they wish. Because this makes more sense for them. So If I select tmta tmtb stroopI StroopII hey appear in the order selected. But if they want to fill out first StroopII then tmta etc they should be able to rearranged by hand. 

### 7. When users are logged in

Selected tests should have a window with ‘most used tests’ for each clinician.
Nothing has been decided about implementation of the login. This feature can be implemented without login with use of browser local storage.

~~### 8. We would like to add introductory text (few lines) on top of this page (short instruction)~~

~~> Welcome to the ANDI portal. On this page you can select the neuropsychological tests you have administered and which you want to analyze. You can browse the tests by category, or search for the tests by using the ‘search for…’ function. Clicking the ‘+’ icon will expand each section. Ticking the boxes will add the tests to the ‘Selected tests’ list, and from here you can arrange the order of your variables.~~

~~> Your data will automatically be compared to the latest version of ANDI. In case you wish to select an older version you can click ‘older version’. Note that we highly recommend always using the latest version.~~

~~> When you have completed the test selection, press `Next` to  go to the next step.~~

### 9. Extra

Allowing clinicians to upload a downloaded excel file of their patients. On this first page you should already allow clinicians to upload data they have previously filled in. You can name this button ‘Upload template from previous session’. This will always be one of our exports (and this have correct variable names). You can crossmatch the uploaded excel with our template. If it is not the same give the warning ‘this file does not seem to be an export from our website. Please construct a template first’. So in that case they will first have to select the tests and only in the second screen can download the template.

## Demographics and data entry

### 10. Rename section

Should be `Data entry`. Entering demographic data is also data.

~~### 11. We would like to add an introductory text (few lines) on the top of the page.~~

~~> On this screen you can add the test values and demographic information for your patients. You can either fill out the table below, or select *"I wish to upload data"*. If you wish to upload your data you can download the `.csv` template in which the test scores can be filled out. After you have saved the file you can upload it to the page by clicking *"choose file"*.  Once the file has been uploaded the screen will ask you to define your missing values. When you submit this page, the website will fill out the table with your information and you can check whether it has done so correctly.  Note that all patients need to have a `unique ID`. At the bottom of the page under *"Advanced settings"* you can change statistical settings.~~

### 14. If someone uploads data using a filled out template file

The tests should be detected from this file, so they do not have to be reselected in the test selection screen.

### 15. The csv needs to be able to be opened on *Dutch excel*

Currently it is not because it is comma separated. This is confusing. So we should either add extra instructions (that they use the import wizard to use comma separated). Dutch setting shoud be the default bot for download and upload.
We will look into option of excel files upload, that will simplify format detection.

### 16. Date conversion

Date should also be in Dutch format, as other things in csv file (requirement 15)

~~### 17. Validate patient ID numbers (need to be unique).~~

~~### 18. When filling out the form the website~~

~~Should check values if possible. Thus if an impossible value is filled out the website should make the box red and ask for a correction (instead of after you’ve clicked `submit`).~~

### 19. Missing values

Where clinicians need to define their missing values (e.g. 999 or 9999 or an empty field), let them fill out multiple values. Call these not `empty fields` but `missing values`.

- update the dialog about missing values when uploading the file (current version is not intuitive)
- missing values should empty values in the table

~~### 20. What is the difference between ‘Submit’ and ‘Next’ at the bottom of this page?~~

~~I would make only `Previous` and `Next`.  By clicking `Next` you automatically submit the form.~~

### 44. Going back to tab 1. 
Clinicians should be able to go back to tab 1 and select more tests while leaving the data in tab 2 in tact.

### 45. Deleting variables in tab 2
From the tab with patient scores clinicians should be able to delete variables (by clicking 'x').

### 46. Computing variables
Some variables are computational. Which means the clinicians will fill out trial 1 2 3 4 5 and the website will do 'sum' for them. 


### 21. The fields

- should have little question marks or *i* symbols to request more information.
 For example we’d like to have a list of `Verhage` education levels under this mark so clinicians unfamiliar with Verhage can still use the system.

- demographics fields in the table should be distiguishable from the test variables 

### 22. Age and birthdate/test years

Should be either one + a little ‘calendar’ to calculate age.

~~### 23. Advanced Settings~~

~~Should have pre-sets (else it is not advanced settings but just settings because everyone has to set them). Also should allow for expanding available iptions for new types of analysis.~~

### 41. Tab for 'statistical settings'.
So what happens is that because we have a lot of different statistics for one neuropsychological test (for example TMTa TMTb but also a difference score or total score) we need clinicians to make a selection in which of the variables they want to do computations. 
For the univariate statistics this is no problem (we can do them on all and let users select what to display in the results section). However, for the multivariate statistics this can be problematic because all these 'computed variables' from the original trials correlate very highly with the other measures. This is not so beneficial for the multivariate statistics so we want to force a choice for the clinicians which are used for these statistics. Also this tab will have all calculations options that they can preselect (do they want univarite or multivariate? etc.). Idealy the 'Advanced Settings' from number 23 will be in this selection tab.

## Results

### 24. Ellipse plots for the MNC

### 25. Results should be exportable
"results" - data used to generate the plots and plots.
It is tricky to export svg plots and might not be feasable.

### 26. The table can also contain data used to generate the plots.

### 27. Raw data should be exportable as well
To `.csv` for example. Ine same way as downloading a template, so that it can be uploaded later.
"raw data" - data entered by a clinician, 

### 42. So after the tab 'Results' we should make a new tab for 'Export'. 
Here we can again let clinicians make choices what tabs and figures and for which variables they want their 'print screens'. This also 'solves' the problem that the plots on the 'Results' section are interactive but the output (word/pdf etc.) needs to be static. So instead of giving them each single plot from the elipse matrix (20x20 for example) they can choose what they want to download.
Here there should also be a box for downloading the patient data (in csv/excel what we mentioned earlier).

## Layout / Look

### 29. Footer

Should always be displayed at bottom of the page (page size be held constant even if it is not entirely filled) (see ANDI.nl).

~~### 30. Header-menu~~

~~Should be deleted. Only header is the ANDI logo.~~

### 31. No lines separating header/body/footer.

### 32. Words/buttons etc.

Can be bigger (similar to ANDI.nl).

### 33. Look should be consistent to ANDI.nl.

## Other / Cooperation with Joost & Nathalie

### 34. Tests with multiple trials

Should be filled in separately. The computer should calculate the total score (and compare it to the score in the normative data). For example, clinicians fill out AVLT1, AVLT2, AVLT3, AVLT4, and AVLT5 the portal calculates AVLTtotal and compares this to AVLTtotal in the database. This needs to be implemented also in the input file. The information about which tests add up needs to be provided.

### 35. Test scores

- Should be comparable pairwise (so comparing whether a score on AVLTtotal is deviant given a score on TMTb). This involves input and output issues as the clinician should be able to select a pair of tests dynamically, on which a comparison is performed. Calculating these for all combinations of tests beforehand is possible (just a little intensive); displaying the results for all possible combinations is not desirable.

- Should be comparable to a group of other tests (so comparing whether a score on AVLTtotal is deviant given scores on TMTb, StroopCW and SemanticFluency). This involves more difficult input and output issues as the clinician should be able to select a combination of one test, and comparison group of tests. Calculating these for all combinations of tests and comparison groups beforehand is practically impossible.
 
Future requirement, assigned to Joost.

### 36. The variable names should be made Dutch (portal can remain English).

### 37. Encryption

For the ‘form sending’ procedure (so when data of patients are uploaded to be compared).

### 38. Portal should always be compatible with all browsers

Even old ones such as IE9.

~~### 39. When adding patients in second tab would it be possible to have a tab for adding patients and a cross to remove the patient.~~

### 40. Two new columns will be added in the the input database file by Nathalie, one representing more information about the variables and the other representing information about dutch alias for a the variable name.

# Requirements added after April 2016
## Upload and download button

- should be in the first tab
- download button should be under selected tests list

## tabs should not be selectable, they should only reflect where you are in the application
## selected tests
- should be a sum of preselected tests and tests from uploaded file
