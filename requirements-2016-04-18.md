# Requirements for ANDI web application

## Input page

### Normative Data

Should not be a drop down menu. Instead it is preselected on the latest version with a small button for ‘older version’ next to it. This will give a pop up in which an older version can be selected.  I would rename this  `Database version`.

### Search for relevant tests

Should be `Search for neuropsychological tests`.

### Tests in tree structure

Should be searchable both by test category (as it is now) as well as by the alphabet.

### Selected tests

Should be removable by a clickable ‘x’ next to the name.

### Selected tests

Should display the entire test + variable name (Long name 1 + Long name 2 + (if needed) Long name 3) from the template.

### Selected tests

Should be drag-able to a preferred order by clinicians.

### When users are logged in

Selected tests should have a window with ‘most used tests’ for each clinician.

### We would like to add introductory text (few lines) on top of this page (short instruction)

> Welcome to the ANDI portal. On this page you can select the neuropsychological tests you have administered and which you want to analyze. You can browse the tests by category, or search for the tests by using the ‘search for…’ function. Clicking the ‘+’ icon will expand each section. Ticking the boxes will add the tests to the ‘Selected tests’ list, and from here you can arrange the order of your variables.

> Your data will automatically be compared to the latest version of ANDI. In case you wish to select an older version you can click ‘older version’. Note that we highly recommend always using the latest version.

> When you have completed the test selection, press `Next` to  go to the next step.

### Extra

Allowing clinicians to upload a downloaded excel file of their patients. On this first page you should already allow clinicians to upload data they have previously filled in. You can name this button ‘Upload template from previous session’. This will always be one of our exports (and this have correct variable names). You can crossmatch the uploaded excel with our template. If it is not the same give the warning ‘this file does not seem to be an export from our website. Please construct a template first’. So in that case they will first have to select the tests and only in the second screen can download the template.

## Demographics and data entry

### Rename section

Should be `Data entry`. Entering demographic data is also data.

### We would like to add an introductory text (few lines) on the top of the page.

> On this screen you can add the test values and demographic information for your patients. You can either fill out the table below, or select *"I wish to upload data"*. If you wish to upload your data you can download the `.csv` template in which the test scores can be filled out. After you have saved the file you can upload it to the page by clicking *"choose file"*.  Once the file has been uploaded the screen will ask you to define your missing values. When you submit this page, the website will fill out the table with your information and you can check whether it has done so correctly.  Note that all patients need to have a `unique ID`. At the bottom of the page under *"Advanced settings"* you can change statistical settings.

### Rename top functions

Should be `I wish to type in data` & `I wish to upload data`.

### If someone uses the top function to select `upload data`

The entire box should be greyed out (also the test names). The `download template` section should move on top.

### If someone uploads data using a filled out template file

The tests should be detected from this file, so they do not have to be reselected in the test selection screen.

### The csv needs to be able to be opened on *Dutch excel*

Currently it is not because it is comma separated. This is confusing. So we should either add extra instructions (that they use the import wizard to use comma separated). But I would opt for using Dutch-settings as a default.

### Date conversion

Perhaps detect the date format that excel automatically uses (this is again different for Dutch/English excel).

### Validate patient ID numbers (need to be unique).

### When filling out the form the website

Should check values if possible. Thus if an impossible value is filled out the website should make the box red and ask for a correction (instead of after you’ve clicked `submit`).

### The pop-up

Where clinicians need to define their missing values (e.g. 999 or 9999 or an empty field), let them fill out multiple values. Call these not `empty fields` but `missing values`.

### What is the difference between ‘Submit’ and ‘Next’ at the bottom of this page?

I would make only `Previous` and `Next`.  By clicking `Next` you automatically submit the form.

### The fields

Should have little question marks or *i* symbols to request more information.

For example we’d like to have a list of `Verhage` education levels under this mark so clinicians unfamiliar with Verhage can still use the system.

### Age and birthdate/test years

Should be either one + a little ‘calendar’ to calculate age.

### Advanced Settings

Should have pre-sets (else it is not advanced settings but just settings because everyone has to set them). Also should allow possibility of expanding this by adding analyses options (which tests are done).

## Results

### Elipse plots for the MNC

### Results should be exportable

### The table can also have the filled out data (raw data).

### Raw data should be exportable as well
To `.csv` for example.

### Plots/results should be downloadable.

## Layout / Look

### Footer

Should always be displayed at bottom of the page (page size be held constant even if it is not entirely filled) (see ANDI.nl).

### Header-menu

Should be deleted. Only header is the ANDI logo.

### No lines separating header/body/footer.

### Words/buttons etc.

Can be bigger (similar to ANDI.nl).

### Look should be consistent to ANDI.nl.

## Other / Cooperation with Joost & Nathalie

### Tests with multiple trials

Should be filled in separately. The computer should calculate the total score (and compare it to the score in the normative data). For example, clinicians fill out AVLT1, AVLT2, AVLT3, AVLT4, and AVLT5 the portal calculates AVLTtotal and compares this to AVLTtotal in the database.

### Test scores

- Should be comparable pairwise (so comparing whether a score on AVLTtotal is deviant given a score on TMTb). This involves input and output issues as the clinician should be able to select a pair of tests dynamically, on which a comparison is performed. Calculating these for all combinations of tests beforehand is possible (just a little intensive); displaying the results for all possible combinations is not desirable.

- Should be comparable to a group of other tests (so comparing whether a score on AVLTtotal is deviant given scores on TMTb, StroopCW and SemanticFluency). This involves more difficult input and output issues as the clinician should be able to select a combination of one test, and comparison group of tests. Calculating these for all combinations of tests and comparison groups beforehand is practically impossible.

### The variable names should be made Dutch (portal can remain English).

### Encryption

For the ‘form sending’ procedure (so when data of patients are uploaded to be compared).

### Portal should always be compatible with all browsers

Even old ones such as IE9.
