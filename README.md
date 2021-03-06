# xm-labs-freshdesk
Freshdesk is a help desk system and customer service solution that simplifies customer service for your team and helps them provide a great customer experience. The xMatters Freshdesk integration is a closed loop integration that notifies on-call response teams and assigns Freshdesk tickets using xMatters responses. 

# Pre-Requisites
* Freshdesk account: Free trials available, request one here: https://freshdesk.com
* xMatters account: Free tiers available for small teams, free forever! Request an xMatters free account here: http://xmatters.com/free-forever

# Files
* <a href="https://github.com/TastyWavez/xm-labs-freshdesk/blob/master/Freshdesk.zip">Freshdesk.zip</a> The workflow containing the flow canvases and event forms.


# How it works
Delight your customers with rapid response times from your support team no matter where they are! The xMatters Freshdesk integration  is a closed loop integration that notifies on-call response teams and assigns Freshdesk tickets using xMatters responses.  xMatters also sends callbacks to Freshdesk in real time so you can know the xMatters event status, annotations and device delivery details. 

Freshdesk automations trigger a POST to xMatters Flow Designer when a ticket is open and unassigned. If the ticket is assigned to a particular team xMatters will map this team to the recipients field and notify members of the assigned team. Once notified team members will have the option to respond assigning the Freshdesk ticket to themselves. If the Freshdesk ticket goes to an In Progress, Pending or Closed status a POST is made to xMatters where the event will be looked up via xmAPI and terminated to prevent additional notifications from going out.

<kbd>
  <img src="media/Screen Shot 2020-10-28 at 4.38.30 PM.png">
</kbd>

# Installation 

## xMatters set up

Log in to xMatters as a Company Supervisor or a Developer - you'll need the permissions granted by these roles to configure workflow.

### Create a REST integration user account

<kbd>
  <img src="media/Screen Shot 2020-10-28 at 1.57.55 PM.png">
</kbd> 


### Import the Workflow
1. Navigate to the Workflows page. Click the Import button and import the <a href="https://github.com/TastyWavez/xm-labs-freshdesk/blob/master/Freshdesk.zip">Freshdesk.zip</a> file.
2. Open the workflow and navigate to the **Flows** tab.
3. Click on the **Ticket Alerts** canvas and then double-click the **Ticket Alerts-FreshDesk-Inbound** HTTP Trigger.
4. Copy the URL and save for later.
5. On the **Forms** tab, click the **Web Service** dropdown next to **Ticket Alerts** and select **Sender Permissions**. Add the REST Integration user created in the previous section.
6. Click the gear icon and choose **Editor permissions**. Add the **REST Integration user** user here as well. e.g. **FD Integration** created in the previous section. You can also add additional editor permissions at this time should any developers or admins require access to the Freshdesk workflow.

### Set up the Freshdesk endpoint
1. In Freshdesk we recommend creating an agent account that can serve as an integration user. Create an agent account and give them the **Administrator** role. Provide an email address where you can receive the activation email. Once logged in as the integration user you will be able to retrieve the API key from the users profile by clicking **Profile Settings**. 


<kbd>
  <img src="media/Screen Shot 2020-10-28 at 5.32.54 PM.png">
</kbd> 


2. In xMatters open the workflow and navigate to the **Flows** tab.
3. Click on the **Ticket Alerts** canvas and then select **Components** in the upper righthand corner choosing **Endpoints** from the dropdown. 
4. Choose the FreshDesk endpoint and provide the base URL as shown below substituting "company" with your instance name. 

<br>
<kbd>
  <img src="media/Screen Shot 2020-10-21 at 2.28.53 PM.png">
</kbd>

<br>
5. Choose **Basic Auth** as the authentication type and provide the API key from your Freshdesk instance as the username. The password is arbitrary so choose any random string of characters you'd like. 

### Create the FreshDesk Agent ID Custom Field in xMatters

## Configure Freshdesk

### Ticket Created Automation Rule

1. Log in to Freshdesk using the Administrator account and select the **Admin** cog. 
2. From the admin tab scroll until you see the **Helpdesk Productivity** heading and select **Automations** and create a new automation rule on **Ticket Created** with the following criteria supplying the HTTP trigger URL from the Freshdesk workflow.

<kbd>
  <img src="media/Ticket_Created_FD/Screen Shot 2020-07-13 at 2.34.35 PM.png">
</kbd> 

<kbd>
  <img src="media/Ticket_Created_FD/Screen Shot 2020-10-28 at 4.20.43 PM.png">
</kbd>

<kbd>
  <img src="media/Ticket_Created_FD/Screen Shot 2020-10-28 at 4.22.33 PM.png">
</kbd>

<kbd>
  <img src="media/Ticket_Created_FD/Screen Shot 2020-10-28 at 4.22.42 PM.png">
</kbd>


3.

# Troubleshooting

