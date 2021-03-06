# Automated Attendance Marker

### Description

A python script to automate the task of logging into the eduserver of NIT Calicut and marking the attendance manually. Many would agree that it is rather a tough task especially for the morning 8'O clock classes. 

---

### Requirements

This script would require Python3 to be installed on your machine/mobile device.
In addition to this it requires the python requests module and BeautifulSoup to be there in your machine.

1. Download and install Python from [here](https://www.python.org/downloads/)

After it has been successfully installed, pip install these modules,

`$ pip install requests`

`$ pip install beautifulsoup4`


And you are good to go...

---

### Usage

There is a **credentails.txt** file. Save your login details in that file as space seperated value.
For example,

`m2xxxxxca my_weak_password`

The **schedule.txt** file must contain the schedule of that day. The format is,

*_TIME_ <SPACE> _COURSE_CODE_*

Enter each course time on a new line.
For example on a certain day the file would look like this,

**08:00 IP\
  12:30 PC\
  13:00 LD\
  14:00 DM\
  17:00 SM**

**Note: Use 24-Hour time format. Otherwise it won't work and don't blame me if you loose your attendance. And please save the schedule in an ascending order of time. This is also must for correct functioning.**

Keep in mind that you have to daily update the schedule.txt file only.

Now from the ***"/Scripts/"*** directory just fire it up with,

`$ python RunScript.py`

---

### Capabilities

Current capabilites of this script are to mark the attendance if a link is available on the course page, if not then wait for 15 minutes for the teacher to upload the link, otherwise assume the class is cancelled and carry on. One thing that might bug you a little is that you have to daily update the **schedule.txt** file to reflect the schedule of that day. Although, in the future changes could be made in the code to allow uploading the whole weeks schedule at once and let the code handle what day to choose from the file. This is not something very hard to implement.

### Disclaimer

The script is highly dependent on the course teachers way of putting the attendance links like in IP there is a static link which doesn't change and new links for submitting appear in that page. If at all the teacher decides to daily push a new link on the course page, the script implementation would have to be changed slightly to adapt to this change. And there will always be a way of getting the latest link for submitting the attendance no matter what or how the teachers do. I just needed you to be aware of this fact.

### A message to the users

If you think it is not working perfectly for you, please feel free to contact me or just raise an issue. You can also take the code and customize it for your own use case.


