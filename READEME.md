# To Do App
Click [here](#updates) for updates

## Business Problem
Employees are always trying to balance work and home life. Some are also trying to manage school. Trying to keep track of all that needs to get done for each area along with any special projects can be daunting.
The To Do application will manage and track all the to dos a person needs to complete for any aspect of their life.

## Desired Outcomes
-	A single location where employees can track to do items
-	Accurate and timely completion of all tasks necessary; fewer forgotten to dos
-	No more lost notes tracking what needs to get done
-	Improve productivity as to do items are completed and not forgotten
-	Automation to populate fields and notify users

## Stakeholders
|  Stakeholder |  Value from Application |
|---|---|
|  User (Me) |  Intuitive, easy-to-use interfaces. Access from desktop, tablet, or mobile. Real time visibility of status through a visual task board. Notifications by Slack. |

## Personas

|  Persona | Privileges  |
|---|---|
|  User (Me) |  Ability to submit new records through the Service Catalog or ServiceNow form and check the status of their existing records. Ability to update existing records and see tasks on a visual task board by status.|

## Inputs

|   Data Source| Data Format  |  Frequency |  Duplicate Data Okay? | What Makes Data Unique? (coalesce)  |  Retrieval Method |
|---|---|---|---|---|---|
|  User input - form | N/A  |  As needed | No  |  Number Assigned by ServiceNow | N/A  |

## Outputs

|  Format | Content  | Frequency  | Recipients  |
|---|---|---|---|
|  Slack | Notification of upcoming to do items  |  Daily |  Value in the Assigned to field |
|  Slack | Summary of upcoming to do items  | Weekly  | Value in the Assigned to field  |
|  Slack |  Summary of completed to do items |  Weekly | Value in the Assigned to field  |

## Processes

|  Process | User  |  Description |
|---|---|---|
|  Set Assigned to field value to current user | Current user  | Set the Assigned to value for the To Do record to the user who created the record.  |
| Send reminder slack notification morning of due date.  | Assigned to  | Check daily for a list of To Do records with a Due date of today. Send a slack notification to each Assigned to.  |
|  Send reminder slack summary at the start of the week for all To Do records due this week. |  Assigned to | Check weekly (Monday) for a list of To Do records with a Due date of this week. Send a slack summary to each Assigned to.  |
|  Send reminder slack summary at the end of the week for all To Do records completed this week. |  Assigned to |  Check weekly (Friday) for a list of To Do records with a Completed date of this week. Send a slack summary to each Assigned to.

Send reminder slack notification morning of due date:

 ![Send reminder slack notification morning of due date:](images/Set%20Assigned%20to%20field%20value%20to%20current%20user.drawio.png)

 Send reminder slack summary at the start of the week for all To Do records due this week:

 ![Send reminder slack summary at the start of the week for all To Do records due this week:](images/Send%20reminder%20slack%20summary%20at%20the%20start%20of%20the%20week%20for%20all%20To%20Do%20records%20due%20this%20week%3A.drawio.png)

 Send reminder slack summary at the end of the week for all To Do records completed this week:

 ![ Send reminder slack summary at the end of the week for all To Do records completed this week:](images/Send%20reminder%20slack%20summary%20at%20the%20end%20of%20the%20week%20for%20all%20To%20Do%20records%20completed%20this%20week.drawio.png)


## Data Model

 ![Data Model](images/Data%20Model.png)

 ## Updates

 - 19/10/2022 - Implemented design initial app design (above)