Workflow Explanation: Appointment Scheduler & Auto-Reminder Agent
This workflow automates the entire process of booking an appointment and sending reminders , without needing any manual work. Here’s how it operates step-by-step:

User Fills the Form (Trigger Step)
The workflow begins when a user submits a form. The form collects:
Name
Preferred Appointment Time
Any other custom fields you added
This step captures the input and passes it to the workflow for processing.
Schedule the Appointment (Google Calendar Tool / Scheduler Agent)
Once the form is submitted, the workflow sends the appointment details to the Appointment Scheduling Agent or directly to the Google Calendar node.
This agent does 3 things:
Creates a new event in the doctor/clinic calendar
Sets the date and time based on user input
If successful, a confirmation message can also be sent/returned.
Generate a Confirmation Message
After the event is created, the workflow prepares a custom confirmation message using the template you provided .
Send Auto-Reminder (Email )
After the appointment is added to the calendar, the workflow sets up a reminder using:
Email
Push notification
(whichever you selected)
You can configure it to send reminders:
24 hours before
1 hour before
10 minutes before
or multiple reminders
This is fully automated and does not require any action once configured.
Optional Branching Logic (Error Handling)
If:
The Google Calendar ID is wrong
The date/time format is invalid
The calendar tool fails
The workflow sends an error message:
“ERROR: Calendar parameter’s value is invalid. Please check the calendar URL.”
This helps you debug mistakes quickly.
