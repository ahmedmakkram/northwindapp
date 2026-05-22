# Northwind Products App

A Fiori List Report app that pulls product data from the Northwind OData service, 
built on SAP BTP as part of the Solex internship assessment.

## Architecture Overview

Three things work together here: a Destination in BTP Cockpit that connects to 
the Northwind service, Business Application Studio where I built and tested the 
app, and Cloud Foundry which handles deployment on BTP.

## Setup Instructions

1. Register for a free SAP BTP Trial at https://account.hanatrial.ondemand.com
2. Subscribe to Business Application Studio and assign yourself the Developer role
3. Create a Destination called `Northwind` pointing to `https://services.odata.org`
4. Set Authentication to NoAuthentication and add these two properties:
   - WebIDEEnabled: true
   - WebIDEUsage: odata_gen
5. Open BAS, create a Fiori dev space and run the Application Generator
6. Connect to `/V2/Northwind/Northwind.svc/` and pick the Products entity

## OData Entity Used

I went with the Products entity — it has fields like ProductName, UnitPrice and 
UnitsInStock which felt like the most realistic thing to display in a list.

## Challenges Faced

The preview kept opening a file browser instead of the actual app. Took me a bit 
to figure out I needed to manually add `/test/flp.html#app-preview` to the URL. 
Also had a Git conflict on the first push which I sorted out by pulling first 
then force pushing.

## Bonus Tasks Completed

None attempted in this submission.

## Screenshots

![Destination Configuration](docs/destination.png)
![BAS App Preview](docs/bas-preview.png)
