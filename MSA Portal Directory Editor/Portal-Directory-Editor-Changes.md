# What is the MSA Portal Directory Editor?
## Background
  The **MSA Staff Portal** allows staff to view a directory of current staff and locations (such as the Stacks and the IT Help Desk) alongside their email, phone number, and additional notes.

  The **MSA Portal Directory Editor** is an application that allows administrative staff to make edits to entries in the directory, so they can add users and locations, and edit names, phone numbers, etc.

# The Assignment
The requirement for this project was simple: 
>Have application save each record after it has been updated by the user automatically

## Implementation + a Concern
### The main approach
While the ask was simple enough, I had concerns that simply implementing it without any safeguards could result in unintentional changes being saved and going unnoticed. To remedy this, I decided to add a **confirmation window** which appears when the user tries to navigate away from an entry without saving (if they made any changes). I also chose to add a **"Settings" window**, where this pop-up could be disabled, should it prove too obnoxious (but could easily be re-enabled if users find they make too many mistakes without it).

**The confirmation window presented the changes made to any fields for an entry**, and asked whether the user would like to continue (saving automatically and proceeding with selecting the next entry they'd selected) or stay and keep making changes.

Of course, the original "Update" button remained intact and functional in addition to these changes.

### Additional features
It felt a little odd to make a settings window with only one setting, though, so I decided to add two more features (which could be enabled/disabled in the settings) to the program to help users avoid making any mistakes:
#### Error Providers
A few of the fields for each entry required validation:
- First Name field
- Last Name field
- Phone Number fields
  - Work Phone
  - Phone Number
  - Cell Phone
  - Home Phone
 
This validation was already implemented, in the respect that you could not save an entry with invalid input in any of these fields, but there was no way for the user to know if the input was invalid until they went to save their changes.

My implementation added **error providers** to these fields. **When an invalid phone number was typed into any of the phone number fields, an error provider would appear** to notify the user that it was invalid. A valid phone number was a 10-digit series of integers, with or without the standard hypens in it.

A valid name was any name consisting of one or more alphanumeric characters. **Any "person" entry had to have both a first and last name** listed, so **if either of these boxes were empty, they would have an error provider show.** Some entries, however, were not people, but locations. If there "Is a Location" box was checked for an entry, it needed only a first OR last name, not both. In this case, the error providers only show if it is missing text from both boxes.

#### Textbox Highlights
I also thought it would be good to have some indication of when a field has been changed, which would **passively remind users** of **when they need to save** an entry, as well as draw their attention in case a field was changed that wasn't meant to be. This addition was not wholly my idea, and came about through a conversation about this application I had with a fellow IT intern, [_Hashem Wahed._](https://www.linkedin.com/in/hashem-wahed-b301aa253)

This feature applied to **all editable fields on the form**, and would **highlight a field when its contents were changed from what was stored in the database.** This makes it easy to know, at a glance, whether an entry needs to be saved, reverted, etc.

## The Issue
|describe the issue that occurred here|
