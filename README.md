# mawLIB

This is a library checkout system for the Resource center that I work in. We deployed it using google sheets. It makes use of scripts, formulas, and web deployed front end. 

Installing the library checkout system is a 5 step process. Each step is broken down into step by step installation instructions. 

It is important that every step is completedy fully. 

The QRC LIBRARY CHECKOUT SYSTEM (QLCS) is a comprehensive system that allows the tracking of QRC media and belongings, notification of availability, and reminder of check in responsibilities to the staff and patrons of the center. It has many moving parts that work together. 

These fives steps only have to be done when you deploy the system, and should never have to be done again unless the working system is copied to a NEW administrative account.



#1) COPYING THE DOCUMENT TO THE WORKING ACCOUNT

	Open source Library file

	Request permissions

	From source library file, give permissions

	From requested account, file - make a copy

	Name appropriately

	Logout of all other email accounts



#2) PROVIDING ADMINISTRATIVE ACCESS TO THE ACCOUNT

	Open file that was just saved

	In the URL bar find the SHEET ID

	https://docs.google.com/spreadsheets/d/1VUCT9N-sAV_CpCZ8Sl0CJW_VG2bUftYnCq4QF-XvZUw/edit#gid=0

	It will be everything in between the /d/ and the /edit#gid=0 places

	This sheet ID is 1VUCT9N-sAV_CpCZ8Sl0CJW_VG2bUftYnCq4QF-XvZUw

	Select TOOLS - script editor

	Click the working_library_code if prompted.

	Ctrl-f to find SHEET ID

	Goto the second one, which should be the VERY bottom of the page.

	Where it says SpreadsheetApp.openById('1VUCT9N-sAV_CpCZ8Sl0CJW_VG2bUftYnCq4QF-XvZUw');

	Replace the numbers and letters inside the (' ') part. Double check this is correct then goto file-save



#3) CREATING AUTOMATION

	Click Edit then select Current Projects Triggers

	Press "+Add Trigger"

		 -Choose which function to run: scheduledreminder

		 -Choose which deployment should run: head

		 -Select event source: Time-driven

		 -Select type of time based trigger: Day timer

		 -Select time of day: 5am to 6am.

		 -Failure notification settings: Notify my weekly

		 -PRESS THE PLUS

		 -Failure notification settings: Notify me immediately

	You can change any of these later.

		-Press save.

		-Select the administrative account

		-A warning will pop up saying this app is not verified

		-Click Advanced.

		-Goto working_library_code(unsafe).

		-Scroll down then press Allow

	You should now see the trigger pop up in the Apps Script page there.

	Press "+Add Trigger"

		 -Choose which function to run: mYFunction

		 -Choose which deployment should run: head

		 -Select event source: From spreadsheet

		 -Select event type: On Edit

		 -Failure notification settings: Notify my weekly

		 -PRESS THE PLUS

		 -Failure notification settings: Notify me immediately

		 -Press save

	Close the triggers window or tab.

	In the Working_Library_Code scripts window, press ctrl-s, or goto file-save.

	Close this scripts window.



#4) GENERATING THE PUBLIC ACCESS PAGE

	In the QRC LIBRARY SPREADSHEET goto file -> publish to web

	Click "Entire Document" and select Public Access -- This step is very important to complete carefully.

	Then select "Web page" and an URL should show. Copy this URL.

	Close "Publish To Web" window by pressing the X

	Goto the DETAILS tab, the red tab at the very end.

	Goto line "11 Public Access" and select box 11C.

	Goto the data entry line (Where it says fx underneath the toolbar) and paste the URL you previously copied.



#5) TESTING THE OPERATION

	In the QRC LIBRARY SPREADSHEET test an entry from the "QRC Check Tab", pressing the "Check In / Out" box for a book.

	Enter in your email, or an email that isnt the same as the account where the QRC LIBRARY SPREADSHEET is living.

	After you enter in all the details you should see the spreadsheet show the students data.

	In the Currently Checked Out Materials tab, you should also see that entry added to the list of checked out items.

# Congratulations, the QRC LIBRARY SYSTEM is now installed and functional.

