# JCF Quick Award v.01
For JC Ink services

Version v.01

## Installation
Add the main file **JCF-QA-Main-File** to your wrapper footer, via include key. Install the activation button (or rebuild it, up to you) as a sibling to the username elements in the *post row* template, if you want it to auto-fill the first name. The username elements of a default template look like: *<span class='<!-- |name_css| -->'><!-- |name| --></span>*

Alternatively, you can drop it in as a sibling next to the username in your existing templates, and append the class *normalname* to the element the contains the username.

or don't, up to you!

You will also need to create a new *textarea* type profile field. The field can be hidden from normal members, but should not be made uneditable. In the main file **JCF-QA-Main-File**, on lines **287** and **288**, the variables **fieldNum** and **templates** must be edited to reflect the field number of your newly created field.

You can also choose to edit the following settings:
*resetFormOnSubmit* : Will clear the input fields and selected award templates of all info upon a successful awarding
*autoAddFirstName* : Will seek out the username in the *.normalname* sibling to *.qaButton*, if it exists
*storeSessionID* : Will store the ACP session ID string in localStorage. Fair warning: this may be exploitable
*sessionTimeout* : This determines the number of minutes from the last ACP login that the stored Session ID will be kept

## Usage
The script appends a menu enabling an admin to quickly hand out awards based off of saved templates, or by creating a new award on the page. The user must strike the enter key while focused on the username input field, or click the check mark, to register an extra username to be awarded. A list of awardees may be viewed by clicking the triple bar 'hamburger' icon to the right of the username input field, and usernames can be struck from the list by clicking the X'd arrow to the right of the name.

Importantly, the status bar at the bottom of the dialog window updates when a connection is made, successful or otherwise. Keep an eye on it if you're not sure if anything is happening.

## Common Issues
*Nothing happens when I hit submit*
Make sure that there is at least one award recipient defined in the list. You can view a list by clicking the triple bar 'hamburger' icon to the right of the username input field.

*No award templates are being loaded*
Click the refresh icon in the top right. If nothing further happens, check for saved data inside the profile field, and check the console for javascript errors.
