

# Calender Description
The Calender Plugin  enables you to manage all events and reminders on Zuri App. It offers endpoints so users can Create events and reminders, update and more.



# UPDATE REMINDERS

## Description: 
This endpoint updates the details of a reminder. The reminder id must be present in the request

```sh
PATH PARAMETERS: event_id(required)
```

## How it works
It works when there is a request(PATCH) made to a particular reminder_id to get the reminder linked to the id.

## HOW TO SET UP THE END POINT
These ways to set up the end point to function properly:
- With the help of python set up django framework
- Create all necessary files like ( url.py  ,serializer.py, views.py)
- Import all needed modules
- It is important you set your database in set up ur database with models.py
- Copy the URL for the update reminder request
-   ‘PATCH'\https://calender.zuri.chat/api/v1/update-reminder/{id}
- Paste it where it is needed in the code which is  the url.py
That is a summary of how the end point is being set up.

## Endpoint
<details>
  <summary> PATCH/update-reminder/{id} </summary>
Zuri Calender Plugin

https://calender.zuri.chat/api/v1/update-reminder/{id}
 </details>

## RESPONSES;
### **-200** Event UPDATED Successfully <br>


### Response Sample
**Content type** <br>
application/json

````
{
"_id": "string",
"title": string,
"date": "2019-08-24",
"time": "string",
"repeat": "DO_NOT",
"all_day": true
}
````

# UPDATE EVENTS
## Description:
This Endpoint creates a new event given a request body of required key-value pairs. Returns ID of a created event.

Request Body schema: application/json

## Parameters
|   Name                |   Data type
---------------------------------------
 	Event title         |   string
 	Start and end date  |   string
 	Start  and end time |   string
 	Time zone           |   string
 	Description         |   string
 	All day             |   Boolean
        Event tag           |   string
 	Event color         |   string
 	Reminder            |   string


## Endpoint
<details>
  <summary> PATCH/update_event/{event_id} </summary>
Zuri Calender Plugin

https://calender.zuri.chat/api/v1/update_event/{event_id}
 </details>


## Response
```sh
201
```
- The resource is successfully updated.


## how to update an event
- Click on Add Event
- Enter event title
- Enter start date
- Enter end date
- Enter start time
- Enter end time
- Select time zone
- All day, True or False
- Enter event tag
- Select event color
- Set reminder date and time
- select enter(update)

## The endpoint is setup using django REST framework
