# What is Early Settlers?
## Background
"Early Settlers" is one of several "special collections" maintained by the Archives. According to the Maryland State Archives Guide to Special Collections, "The Special Collections Department, started in 1935, supervises the care, preservation, accessioning, and description of non-state agency generated records (see Code State Government Article, sec. 9-1010). These records are acquired as gifts or deposits by private donors and generally consist of personal letters, diaries, organizational records, newspapers, photographs, maps, and documents. The department also manages the State battle flag collection."

The Index to Early Settlers is a website created and maintained by the Maryland State Archives, intended to allow members of the public to look up early settlers of Maryland by name and other information.

# The Early Settlers Project
"Early Settlers" is the "starter" project that all MSA interns are given. It works with a backup/dummy database and is intended to be a means of getting new interns acquainted with Visual Basic .NET, Visual Studio, and ASPX webpages, as well as the general structure of the internship and code guidelines and expectations at the Archives.

The project given to interns is broken down into two sections: the application, and the ASPX page.
## The Application
The first part of the project is building a Windows Form Application, using the 4.8 .NET Framework, designed to allow Archives staff to access and edit the Early Settlers database.

The following are snippets of the actual instructions I was provided for this project:
>The first things you should add are a ToolStrip control to the top and a Split Container to the middle, so that the different parts of the application can be split up accordingly. Set the “Dock” Property to “Top” and “Fill” to each, respectively.
>
>For the toolbar, add a drop down button labeled “Menu”.  In the “Menu” drop down, add the following buttons: “About, “Settings”, and “Exit”.
> * The “About” button should bring up a dialog box to show the Version number of the application, which you can get through the “My.Application.Info.Version.ToString” method, as well as a short description of the program.
> * The “Settings” button should just bring up another Form that you need to create.  This form can be empty for now.
> * The “Exit” button should close the program down.
>
>Adjust the top half of the Split Container to be about 75% of the screen.  Here you will add a DataGridView, for Archivists to be able to see the data.  The bottom half of the screen should have several TextBoxes with Labels, as well as three buttons: “Refresh”, “Clear” and “Save”.
>
>The Textboxes and Labels should match the fields of data from the Early Settlers’ website, such as “First Name”, “Last Name”, and “Description”.
>
>Add an ErrorProvider to the form.  Use this control’s properties to attach it to the two “Name” TextBoxes.  You will set up functions for the ErrorProvider to show an error if any non alphabetical characters are given in the appropriate TextBoxes.
>
>The three buttons should have the following functions:
> * Clear: Empty all TextBoxes (Use String.Empty)
> * Refresh: Calls Clear button’s function and calls another function that gets a new set of data from the database
> * Save: Uses the TableAdapter to Update records or Insert new records
>
>The text boxes should autofill based on the selected row of the DataGridView (DGV).
>
>The user should not be able to directly change the content of the DGV. All Update and Insert data should be taken from the text boxes and updated/inserted using the Table Adapter functions.
>
>You should also create a function to prompt the user with the option to save when the form is closing so they don’t accidentally lose things they were working on.
>
>Once you have all the controls on the form, play around with the “Dock” and “Anchor” properties of each so they remain visible and in proper locations as users adjust and resize the form.
>
>Once your dataset is prepared, right-click the TableAdapter and select "Add Query" to change the Select command to not bring back fields that are not relevant to the archivists.  Also, try to create the Insert and Update commands to be used when a user clicks “Save”.
>
>Your ultimate goal for this project is to create a data editing application that inserts and updates the data in the database.

## The ASPX Page
The second part of this project is recreating the actual early settlers website <http://earlysettlers.msa.maryland.gov/> as an ASP.NET Web Application.

The following are snippets of the actual instructions I was provided for this project:
>Review the website for its functionality and convert that functionality to an ASPX page. This assignment simulates a typical website conversion. For web work you must use Stored Procedures to interact with the DB for security purposes.
>
>Once you have submitted your second project with the basic functionality and are waiting for review please attempt to improve the functionality and the appearance of your new Early Settlers ASPX.
