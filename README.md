# hue-clip-api.node-red-flows

Hey,

this small respository is actually just an example Flow.
It includes everything you need to communicate with your HUE-Bridge directly using https-request via API V2 (CLIP API)
You wont be dependent on badly maintined contribs anymore, controlling your lamps.

Thanks to user ralfhille, who created the header node!


This flow has one contrib, that need zero maintainance! 
------------

https://github.com/yadomi/node-red-contrib-philipshue-events

Thanks to yadomi making this one!

Before importing my Flow, it is important to install yadomi´s contrib first!
---
DEPLOYING THE FLOW WITHOUT THIS CONTRIB CAN LEAD TO A BOOT LOOP OF YOUR NODE-RED!!!
---

Import the Data from the >>>>>  HUE-CLIP-API_Node-Red-Flows.json <<<<< into a new Flow Tab, AFTER YOU READ THE FULL README!
                              
The Flow has a lot of Comments, it should be easy to figure everything out.
Depending on how much lights you have, this can take a reasonable amount of time to set it up...
But believe me, its absolutely worth it!

First you need to fill in your Data in the Nodes, after that you need to discover your device ID´s and RID´s.
You are doing this using the specific Inject Nodes for the Endpoints you want to disscover, then unfold the whole payload.
The Name of everthing you have given in the App, will be in the Metadata payload, so you know, which ID you just discoverd.

The additional two Files cotain seperately the Sub-Flows and the change nodes with different actions. These are already included in the main File.
It might come handy to import these again in some situations.

Colors get more complicated. These are x/y values now. To determine the right value i recommend to cahnge the color in the app and watch the Event stream.
Open the payload until you find the x/y values and use these. In general in recommend to trigger scenes and not controlling seperate lamps.

I attached some pictures how the flows / payload / xy Color look like.

For a full API Documentation you cloud create an Account at: https://developers.meethue.com/

Hope if some of you can end the struggle with not working contribs!
If you need help, pull a request or start a discussion, Thanks!



Main Flow:
------------
![HUE-CLIP-API](https://user-images.githubusercontent.com/76150626/174089776-de923d78-48eb-4a4b-9b53-53bc0f88ce3e.PNG)

-----------------------------------------------------------


Sub-Flows:
---
![subflows](https://user-images.githubusercontent.com/76150626/174089869-b67e6d15-8ba7-4ab2-8b22-57a2dc43b39e.PNG)

------------------------------------------------------------

Action Change Nodes:
---
![change nodes](https://user-images.githubusercontent.com/76150626/174089961-f4e00eb9-8726-44b9-8d44-d422000f133e.PNG)

-----------------------------------------------------------

x/y Color:
------------

![IMG_2176](https://user-images.githubusercontent.com/76150626/174091836-1fad1f1d-dd5f-479e-b3ee-bf6b25c18eff.PNG)


Lamps:
-------

![light](https://user-images.githubusercontent.com/76150626/173955018-5741e7fb-ef3d-42c7-8629-99135bcef0ab.PNG)

-----------------------------------------------------------

Rooms/Zones:
------------
![rooms](https://user-images.githubusercontent.com/76150626/173955041-0097529e-0e40-4473-b7d4-28fe3282b258.PNG)

-----------------------------------------------------------

Motion:
------------
![motion](https://user-images.githubusercontent.com/76150626/173955078-c922dcb2-ad4c-4501-b574-07f4d8da416a.PNG)

-----------------------------------------------------------

Scenes:
------------
![scene](https://user-images.githubusercontent.com/76150626/173955095-50fd8649-7bf1-4074-bd7f-7624cbffb7c6.PNG)
