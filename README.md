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

# Installation 

## xMatters set up

### Create a REST integration user account

<kbd>
  <img src="media/Screen Shot 2020-10-28 at 1.57.55 PM.png">
</kbd> 


### Import the Workflow
*

### Assign permissions to the Workflow and Form  
*
*
*
*



### Configure xMatters Flow for Inbound REST
*
*
*
*

### Configure Endpoints 
*
*
*
   
|                                 |                                                                     |
|:------------------------------- |:--------------------------------------------------------------------------------- |
|                                 |                                                                                   |


## Configure Freshdesk

# Troubleshooting
*
*
