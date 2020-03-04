# Teaching App - Design Document v3
# Registration
List of emails can be imported as an Excel file and an account is automatically created. Users will receive an email with an activation link. A password can be created when clicking on the activation link. On first login, users will be prompted for their name, level of training and school of anaesthesia (form fields can be prefilled if information is provided in the Excel file - users would just need to check and confirm).
 
## Personal details stored on the server
* Email address (last part encrypted via sodium cryptography) – used as username when logging in
* Password (encrypted using bcrypt algorithm)
* First and last name – can be used by admins (ie at ARCP) to look up attendance record for a trainee
* Level of training – required to filter teaching programme (new starter, core, intermediate, higher)
* School of anaesthesia – required to filter teaching programme (north school, south school)
# Trainee
## 1 Add Teaching Event
## 1.1 Navigate to the Teaching tab
* Use the “Hamburger” menu in the top left corner, then select “Teaching” from the menu, or
* Click on “View North West teaching” in the “My Events” card, or
* Click on the second icon in the bottom Tab Bar
 		 
## 1.2 Select the correct school and training grade
Users select their default school and training grade when registering their account. The list of teaching events is filtered based on what the user selected on registration. This can be changed by clicking on the dropdown boxes (see screenshot). This is useful for trainers and admins as they can quickly look at the teaching programs for different schools and training grades.
 	 
If a trainee moves to a different school or progresses to the next training grade, they can change the default value by ticking the “Save as default” checkbox. This currently requires an internet connection.
## 1.3 Choose a teaching event from the list
* The list of teaching events will show events from -3 days to +12 months.
* Clicking on an event will open a dialog box with event details:
	* Title of event
	* Tutorial (if present)
	* Date
	* Location
	* CPD points and type
	* Any special instructions (if present)
## 1.4 Click on “Add to events” in the dialog box
* Clicking on “Add to events” will close the dialog box and add the teaching event to the trainees account. If the event has already been added, the button will display “Remove from events”.
* In the teaching tab, events added will be marked as “Added to events”.
 	 
## 2 View Teaching Event
* On the home screen, recent teaching events added can be viewed in the “My Events” card.
* A toggle button will show a list of “Previous” and “Upcoming” events.
* Each list will show FIVE events only.
* Clicking on an item will show more details about the teaching event.
 


* To view a list of all teaching added, the trainee needs to navigate to the “Events” tab. This can be done by
	* clicking on the Hamburger menu,
	* clicking on “View all your events” in the “My Events” card or
	* clicking on the third icon in the bottom tab bar.
 	
* The “Events” tab will show all teaching events added by the trainee. By default, only events that took place in the last 30 days are shown. The date range can be changed by clicking on the date range in the table header. This will also allow trainees to view their upcoming events.
 	 
* Clicking on an event item will show more detailed information about the event, such as name of the tutor(s) and number of people attending.
 
## 3 Submit Feedback
* Once attendance has been confirmed by the trainer, the feedback card will show up on the dashboard.
* The feedback page can also be opened by navigating to the teaching tab. When scrolling to the teaching event, there will be a “Submit feedback” button underneath the relevant teaching session.
 	 
* The feedback page has 5 sections
	1) Event details
	2) Trainee can select from a list of 13 words to describe the teaching session
	3) Free text form to allow trainee to give feedback on what went well/what could be improved
	4) Free text form to allow trainee to list their learning points.
	5) Last section allows trainee to rate the teaching session
 	 
 
# Trainer
* Once an admin adds a trainer to the teaching session, it will show up in their events. Just like trainees, trainers can view their teaching events by
	* Going to the My Events card on the home tab
	* Navigating to the “Events” tab
	* Navigating to the “Teaching” tab. When scrolling to the teaching session, it will show ”You are teaching” underneath the teaching session.
 
* Clicking on the teaching event will bring up the event page:
 
* Trainees can be marked as “Did not attend” and “Attended” by using the buttons shown below. Buttons will become active once one or more trainees are selected.
* The “Confirm all” button is active all the time and allows the trainer to mark all trainees as attended, without selecting each one. This will not affect trainees who have already been selected as “Did not attend”. If they have been marked as did not attend by mistake, the trainer has to select the trainee and click the “Confirm” button.
* If required, trainers can download an attendance sheet as a PDF file and print this if required. If the app has been installed on an iPhone, the PDF button will email the PDF file to the trainer as Apple do not allow opening PDF files on installed web apps.
 	 	 
* The event page will also show the feedback provided by trainees for the teaching session. Trainer must mark trainees as attended for them to be able to submit feedback. Feedback provided is anonymous and there is no way to allow admins or training leads to trace back feedback to a trainee.
* Feedback can be downloaded as a PDF file. If the app has been installed on an iPhone, the PDF button will email the PDF file to the trainer as Apple do not allow opening PDF files on installed web apps.
 

# Appendix
Item 1: event is in the past, event added by trainee, attendance confirmed by trainer, feedback completed by trainee
Item 2: event is in the past, event added by trainee, attendance confirmed by trainer, feedback NOT complete by trainee
Item 3: event is in the past and trainer has NOT confirmed attendance
Item 4: event is in the future and trainee added event
Item 5: event is in the future and trainee has not added event
 
Image: Possible states for a teaching event when a trainee visits the teaching tab
21 Jan: Trainee has completed feedback
23 Jan: Feedback is outstanding
24 Jan: Trainee has not attended
28 Jan: Trainee is planning to attend
4 Feb: Trainee is not planning to attend or has not added event yet
(Not shown: ”You are teaching”)
