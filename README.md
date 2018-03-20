# Welcome to post.odkForms!

**GETTING STARTED TUTORIAL:** 

By the end of this tutorial, you will be able to… 
* Create a form standard
* Fill a form, created by a form standard
* Upload the form onto the development server.

# Things to Know:
### Production Code:
Production Code is the code you are shipping out, which deals with customers (i.e new version of Facebook).
This is the code that is running on the customer’s device.
*IMPORTANT*: Be very careful with production code because you do not want the customer to have errors. 


### Development Server vs Production Server:
*Development server*: the server you send your product to be tested.

*Production server*: the server that customers use (you want the product to have little errors here).
*IMPORTANT*: Most of the testing is done in the **development server**.


### APPSPOT:
Appspot is a Google engine that our server is running on. 


### ODK Aggregate:
ODK is a google-created open source set of tools that helps organizations collect and arrange data. 
We will be using ODK to collect plant data from operators. We use ODK because it can be used in areas
where there is not internet connection, which works for us because the areas where our plants are located
don't always have internet connection. Learn more about ODK and access tutorials [here](https://opendatakit.org/).


### XLSForm: 
XLSForm is a tool that allows people to create a form standard through Excel. In other words, it provides a format to 
structure forms. When you open the Excel file, you should see two basic worksheets: survey and choices. The survey worksheet
structures the form and contains the content the form. The choices worksheet specifies the possible answer choices for 
multiple choice questions.

**Please read [THIS](http://xlsform.org/) to gain a stronger understanding of XLSForm and the basic formatting. 


### Headers:
In the XLSForm, you will see the headers type, name, and label. Type is the kind of data that the user is entering. 
You can find a list of basic types [here](http://xlsform.org/#question-types). Name is just the variable name. Make 
sure there are no spaces in the variable name. Label is the text that the user will see (i.e the question)


### Worksheets:
There are two types of worksheets; the survey and choice. The survey gives the overall structure and contains most of the 
content (the type, name, label). The choice sheet is used specifically for the multiple choice questions. There, you will
specify the choices you have. Refer to the website for more information and how-tos.

# Application
## Setup:
### What to Download:
Download “xlsform offline” → first link on Google (gumroad). It will ask for a donation but you can put 0 for the donation.
XLSForm offline converts your created xls form and converts it to an xml version.

### Navigate to Development Server:
Open Aguaclara Google Drive → Active Subteams → Plant Operation Smartphone Tracker (POST) → Archive → Management → 
Passwords/Certs → POST Passwords. 

Go to Development and Production Aggregate Servers section of the document
* You can log into the development server using the administrator login information on the document

### Cloning the Repository:
Go to the POST Github repository and clone it. You can find how to clone a repository [here](https://help.github.com/articles/cloning-a-repository).

### Download the POST Collect APP:
Using an android device, download the Post Collect app through the play store. The app we are running is a fork of the
actual ODK collect app. The reason why we fork it is because we change the app and need to update the app in the future.

Once downloaded, open the app and go to General Settings (3 dots on the top right) → Configure platform settings and 
change the url to the link of the development server in the POST password document. No need to touch username and password.

## Start Formatting:
### Save the file:
Open an existing xls form from your local repository and save the form using save as. Make sure the file format is 
Excel 97-2004 Workbook (.xls), **not** .xlsx. Clear the data (for future uses, just change the data directly). 

### Fill it in:
Fill in the XLSForm with the types and labels you want. Save it in the end. 

### Convert to an xml File:
Using the xlsform offline program that you downloaded in the beginning, select the xls form that you wrote. 
Make sure “validate converted XForm with ODK validate” is checked. Check that it worked by looking up the file and 
opening it. 

### Adding a Form Standard:
Go to the Aguaclara development server (under “Navigate to Development Server”)

Click LOGIN in the upper right corner of the webpage.

Click “Sign in with Aggregate password”.

Fill in the username and password given in the Post Passwords Google Document, under Site Administrator. 

Once you login, under Form Management tab, click “Add New Form”. 

Upload the desired form standard into “form definition”. Make sure the file chosen is a xml file, not xls.

Once you upload your form, make sure it is downloadable and that it accepts submissions if needed.

### Testing Your Form!
This is the exciting part because you get to test the form you created. Open the Post Collect app (you should’ve configured
the settings before) and get a blank form.

Unselect all the forms except the one that you just added. Once you get a success, it should return to the home page. 

Select fill blank form, and click the form you just got. 

After you finish filling it, go to send finalized form to send the form. Now you are good to move on to the next step.


### To View Data:
Under the Submissions tab, you can view the different forms sent in by the “operators” (in the development server, these forms 
will be your own test forms). 

To do so, you must select which form standard you want to view by clicking on “Form”. This will load all the forms sent
in using the particular form standard and list the information in each form. Select the desired form. 

Under From Management, you can view the different form standards that is on the Aguaclara Server. 
