To open the Osler demo project please follow the steps below:
1. Open the Business Space of WBE by clicking start>All Programs> WebSphere Business Events v7.0.1>Business Space.

2. Enter the User ID and the password
	-User ID: Aladdin_baarah
	-Password: 2611

3. Create a new space for the demo.
	-Click the “Manage Space” text link in the top left of the page.
	-Click the “Create Space” button.
	-Type the name of the space (i.e. OslerDemo) and hit save.
	-Click “Done” button.
	-Now you are in the OslerDemo space.
	-Click “Go to Spaces” text link in the top left of the page and then choose the OslerDemo space.

4. Click “Edit Page” button located at the center of the page.

5. Drag two widgets onto the page from the palette, namely, Business Event Design and Business Events Tester. 

6. Add first the Business Events Design widget by clicking the “+” sign next to it.
	-Click the “Project” menu and choose open.
	-Under the Folders section choose "Open Local.xml file"
	-Choose file which is located at C:\Osler Demo\OslerExtendedScenario_V4(Demo)
	-Enter a new folder to be created and name it "Osler Demo"
	-Enter a name for the project and call it "OSler Demo"
	-Click “Runtime” menu and choose “Delete repository assets” and then click OK
	-Click again “Runtime” menu and hit “Publish to runtime”

7. Add the second widget “Business Events Tester” from the palette by clicking the “+” sign next to it.
	-You have to restart testing by clicking “Restart testing” button.

8. Before running the connectors, which listens to the events from the folder “C:\OslerProject\TestCase1\InputEvents” and write the actions (.XML file) in the folder “C:\PFM\apache-tomcat-7.0.23\webapps\PFM\xml” (files consumes by PFM and forwarder to MSG Broker), remove any files reside in the Input folder for the WBE located at “C:\OslerProject\TestCase1\InputEvents”.  

9. Run the connector by clicking start>All Programs> WebSphere Business Events v7.0.1> Connectors.
	-You are asked to enter the user identity and user password.
	-User Identity:Aladdin_baarah
	-User Password:2611


10. Now, WBE is ready for receiving events, through the input folder “C:\OslerProject\TestCase1\InputEvents”, from RTLS and BPM.

11. Make sure both the input folder “C:\OslerProject\TestCase1\InputEvents” and the output folder “C:\PFM\apache-tomcat-7.0.23\webapps\PFM\xml” are open and they are 	in front of you.
	-This helps in monitoring input events to WBE and monitoring inferred events that goes to the output folder. NOTE: This is crucial for troubleshooting. See 		troubleshooting section

12. When WBE receives events from BPM or RTLS, it consumes those events from the input folder. 
	-Double check the “Context Data” in the tab of the Business Events Tester widget which proofs that WBE receives the input event.

13. When WBE generates an action (Inferred event), it writes that event (.xml) in the output folder “C:\PFM\apache-tomcat-7.0.23\webapps\PFM\xml”.
	-Double check the “Action” in the tab of Business Events Tester widget. You can see the desired output events there.
	-Click Refresh button inside the widget in case you couldn’t see the output.  
	-Double check that the action is logged as well in the Console of the MSG Broker
		-Go to the MSG Broker Console by typing the URL: http://137.122.88.139:8080/osler-mb/
		-Under “Log Anaytics”, click “Incoming Log” text link.
		-Refresh the page each time WBE generates the output event.


