*This script was written quite some time ago, utilizing no external libraries. It uses an iterative search instead of a HTML Parser to extract data from the file.*

This script is written for use in Jaypee University of Engineering and Technology, India. The usage is quite simple, with calling the funtions with the username and passwords as arguments.

A demo can be seen at the following link, replacing `username` and `password` with your credentials:
[http://juetapi.sidverma.net/attendance/`username`/`password`](http://juetapi.sidverma.net/attendance/username/password)

###Difference between Attendance and extended Attendance.

####Attendance

This script fetches the Attendances only and displays the info in JSON format.
Usage : `getAttendance('username','password')`

	{
        "attendance": {
            "lecture": "85",
            "lectut": "88",
            "practical": "N/A",
            "tutorial": "100"
        },
        "link": "ViewDatewiseLecAttendance.jsp?EXAM=2014EVESEM&REST=REDACTED",
        "subject": "MICROPROCESSORS AND CONTROLLERS - 10B11CI401"
    }

####Extended Attendance

This script fetches the Attendances and also the details of all the subjects from their respective pages and displays the info in JSON format. This script takes longer to fetch as it has to open every subject's individual page.
Usage: `getExtendedAttendance('username','password')`

	{
        "attendance": {
            "lecture": "85",
            "lectut": "88",
            "practical": "N/A",
            "tutorial": "100"
        },
        "extradetails": {
            "absents": 3,
            "lastAbsent": "19-02-2014",
            "lastClass": "21-02-2014",
            "presents": 24
        },
        "link": "ViewDatewiseLecAttendance.jsp?EXAM=2014EVESEM&REST=REDACTED",
        "subject": "MICROPROCESSORS AND CONTROLLERS - 10B11CI401"
    }

*Please give credit where's due, in case you ever use this.*
