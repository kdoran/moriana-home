# Windows 10: Start CouchDB on Startup

CouchDB can fail to start on computer restart when installed as a service on Windows 10 (and potentially other windows), even when configured to start automatically.

1. Click "Start" and type "Services". You should see this:

  ![Alt text](startmenuservices.png?raw=true "Start Menu Services Screen Shot")

2. Click on services and you should see this:

  ![Alt text](services.png?raw=true "Services Screen Shot")

3. Right click on the service called "Apache CouchDB". Click on "Properties"

  ![Alt text](couchdbpropertiesrightclick.png?raw=true "CouchDB Properties Right Click Screen Shot")

  ![Alt text](couchdbproperties.png?raw=true "CouchDB Properties Screen Shot")

4. Change "Startup type" to "Automatic (Delayed Start)":

  ![Alt text](automaticdelayedstart.png?raw=true "Automatic Delayed Start Screen Shot")

5. Next, click on the tab named "Recovery":

  ![Alt text](recoverytab.png?raw=true "Recovery Tab Screen Shot")

6. Change all three options that say "Take No Action" to "Restart The Service":

  ![Alt text](restarttheservice.png?raw=true "Restart The Service Screen Shot")

7. Then change "Restart the service after" from 1 minute to 5 minutes:

  ![Alt text](afterfiveminutes.png?raw=true "After 5 minutes screen shot")

8. Confirm you changed the options for First, Second, and Subsequent failures to "Restart The Service". WARNING: they should NOT be set to "Restart the Computer", that could damage your system.

9. Save & restart the computer. 10-15 minutes after starting up, go to http://localhost:5984/. You should see a "Welcome" response if everything was successful.
