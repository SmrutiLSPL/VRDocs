
# Dispatch system from reservation
<procedure title="Dispatch Functionality for Inspection Tasks: " collapsible="true">
    <step>Dispatch functionality for inspection tasks refers to the system's capability to coordinate and manage the inspection process within a facility, such as hotels, resorts, or commercial properties. This functionality facilitates the assignment and tracking of inspection assignments to designated inspectors or inspection teams responsible for assessing the quality, cleanliness, and compliance of various areas or assets within the facility. It involves the systematic allocation of inspection tasks, scheduling of inspections based on predefined criteria or intervals, and the ability to monitor the progress and results of inspections in real-time. Dispatch functionality for inspection tasks enables efficient coordination of inspection activities, timely identification of issues or deficiencies, and proactive measures to maintain quality standards and compliance requirements within the facility.</step>
</procedure>
<procedure title="Dispatch Functionality for Housekeeping Tasks: " collapsible="true">
    <step>Housekeeping refers to the management and maintenance of a living or working space to ensure cleanliness, orderliness, and functionality. 
          It involves a variety of tasks such as cleaning, organizing, tidying, and maintaining the overall condition of a space. 
          Housekeeping encompasses both routine chores like sweeping, dusting, and laundry as well as more specialized tasks like Check Out Clean,Deep Clean,Initial Clean and Re-Clean . Effective housekeeping not only promotes hygiene and safety but also contributes to creating a comfortable and pleasant
          environment for occupants or visitors. In commercial settings, housekeeping may also extend to the maintenance of public areas, facilities, and equipment to uphold
          cleanliness standards and enhance the overall experience of customers or users.</step>
<step>Dispatch functionality for housekeeping tasks refers to the system's capability to efficiently assign and manage cleaning assignments within a facility, 
such as hotels, resorts, or commercial properties. This functionality streamlines the process of allocating specific cleaning tasks to individual housekeeping staff members based on factors such as room occupancy, task urgency, staff availability, and task priority. 
It involves the systematic distribution of cleaning assignments, real-time tracking of task status, and the ability to reassign tasks as needed to optimize workflow and 
ensure timely completion of housekeeping duties. Dispatch functionality for housekeeping tasks enhances operational efficiency, facilitates effective 
communication among staff members, and ultimately contributes to maintaining cleanliness and orderliness within the facility.
</step>
</procedure>


<code-block lang="mermaid">
flowchart LR
   A[Reservation]
   A ----> B[Disptch View ]
   B----> C[Inspection Task]
   B----> D[Housekeeping Task]
   
</code-block>

# Inspection work-flow
Narrative:
As a hotel manager or staff member responsible for ensuring the quality and cleanliness of guest accommodations, I need a systematic way to conduct room inspections. This will enable me to promptly identify any issues or deficiencies, maintain high standards of cleanliness and presentation, and ultimately enhance the guest experience.
- Access to Inspection Module: The system should provide access to a dedicated inspection module that allows authorized users, such as hotel managers or staff, to conduct room inspections.
- Unit Selection: Users should be able to notify the specific room or rooms to be inspected from a list of available accommodations within the hotel on Check-In day of user 
- Checklist Creation: The system must allow users to create or select a predefined checklist of inspection criteria to be used during the inspection process. This checklist should cover essential aspects such as cleanliness, maintenance.
- Conduct Inspection: Users should be able to systematically conduct inspections by going through each item on the checklist and assessing the condition of the room accordingly.
- Issue Identification: During the inspection, users should be able to identify and document any issues, deficiencies, or maintenance requirements encountered in the room, providing detailed descriptions and optional photo attachments if necessary.
- Severity Classification: Users should be able to classify the severity level of identified issues (e.g., minor, moderate, severe) to prioritize and address them accordingly.
- Resolution Tracking: The system should allow users to track the resolution of identified issues, including assigning tasks to relevant staff members, setting deadlines for completion, and updating the status of each issue as it is addressed.
- Reporting: Users should be able to generate comprehensive inspection reports summarizing the findings, including a list of identified issues, their severity levels, status updates, and any associated actions taken or Hold the unit .
- Rationale: This user story addresses the need for a streamlined and efficient inspection process within the hotel's operations, enabling staff to systematically assess room conditions, address any issues promptly, and maintain high standards of quality and guest satisfaction.


# Housekeeping work-flow
- Task Creation:  The system must allow users to create a list of cleaning tasks to be completed before the new client check-in
- Frequency Setting: Users should be able to specify the frequency at which each cleaning task needs to be performed (e.g.,on the day after checkout).
- Date Configuration: Users must have the capability to set the cleaning task, including specific days.
- Task Management: Users should be able to easily edit or delete scheduled cleaning tasks as needed, providing flexibility in managing their cleaning schedule.
- Notification System: The system should send notifications or reminders to users when it's time to complete a scheduled cleaning task, helping them stay on track with their housekeeping responsibilities.
- Task Completion: Users should be able to mark cleaning tasks as completed once they have been finished, allowing for accurate tracking of task completion status.
- Task History: The system should maintain a history of completed cleaning tasks, enabling users to reference past activities and track their housekeeping efforts over time.
- User Interface: The interface should be designed to be user-friendly and intuitive, facilitating easy navigation and efficient task management for users of varying technical proficiency.


| Objective    | To ensure that the dispatch system correctly updates housekeeping tasks on the checkout day and inspection tasks on the check-in day and the same work when the reservation dates are modified.                                                                                             |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prerequisite | * A reservation is created from March 23rd to March 27th.        <br/> * Housekeeping tasks are scheduled for March 27th (checkout day) and inspection tasks for March 23rd (check-in day).     <br/> * User modifies the reservation dates to a new range (E.G. March 25th to March 29th). |

<img src="image.png" alt="Alt text" width="600"/>


<procedure title="Housekeeping tasks are scheduled for March 25th." collapsible="true">
<img src="image_1.png" alt="Alt text" width="600"/>
<tip>
    <p>
    Housekeeping details will appear on the screen the day after checkout. 
    </p>
</tip> 
</procedure>

<procedure title="User modifies the housekeeping schedule." collapsible="true">
<img src="image_2.png" alt="Alt text" width="400"/>
<tip>
    <p>
        The dispatch system should update the housekeeping tasks to March 26th (new checkout day)
    </p>
</tip> 
</procedure>



