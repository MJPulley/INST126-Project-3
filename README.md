# INST126-Project-3
## Michael Pulley
### For Project 3, we are given the task to analyze a log file which contains various forms of information about 50 different users, and with this information we are to generate automated reports. The log file consists of rows and columns of information about the users. The first column in each row represents the "Date and Time" of the activity, in which is separated by a space. The second column of each row represents the "User Activity", which includes "login" and "logout". The third column of every row represents the "Server" from which the activity of the user has occurred. The user activities correlate with 3 different system servers, including "mailserver.local", "myworkstation.local", and "webserver.local". The fourth and final column gives the specific Email-ID of the user. There are 4 different reports that we have to generate from the information provided by the log file. The first report that we have to generate is a "Suspicious Activities" report (suspicious_report.txt). For this report, we have to record if any user logs into any of the systems more than 5 times in a single day, or if the user logs into any of the systems between 12:00 am to 5:00 am. If any user does any of these, it will be marked as suspicious behavior. The second report that we have to generate is an "Irresponsible Behaviors" report (irresponsible_report.txt). In this report, we are given the task to check if the number of logins is greater than the number of logouts for a certain user on a given day. If the number of logins is greater than the number of logouts, it can be marked as an irresponsible activity. The third report that we need to generate is a "System Glitch" report (glitch_report.txt). For this report, we have to record the opposite of the "Irresponsible Behaviors" report tasks. That is, if the system records a greater number of logouts than the number of logins for any user, we mark it as a system glitch. The fourth and final report that we are required to generate is a "Domain Count" report. In this report, we are to generate a list of all the unique domains, as well as the number of users registered within each domain.
### For each report, we were to create a flowchart that describes the process and analysis of how to solve the given problems. These flowcharts give us a visual representation as to how our code should be written and programmed. The flowcharts being created for each report will specifically assist the user through the process of the code, so that they can see how it works and what functions, operators, iterations, etc. work together. 
### In order to generate each report, code needed to be implemented through Python. I began by opening the userlog.log file and utilized the readlines function in order to read the file. I then defined the function "parseLog" with the parameter "logs" and creted a dictionary under the name "logs_dict". Included in this dictionary was the date, time, activity, server, and email, which were all labeled as the different elements. I then used the "append" and "sort" functions in order to format to reports and organize these elements. After that, I defined the function "writeReport" with the parameters "title, fileName, suspiciousAct, suspiciousCount, logs_dict". I utilized iterations and conditional statements to continue to fomrat the reports further. For the suspicious activity code implementation, I started by creating a dictionary called "suspiciousAct", and also created a "suspiciousCount" which equaled to 0 to begin with. I utilized iterations in order to create expressions for the "loginCount" and for those who had a late login (hasLateLogin). Additionally, I used conditional statements to show those who have recorded more than 5 logins, or had a late login. If either of these were true for any of the users, the "suspiciousCount" would increase by 1 (+= 1). I used the "append" and "sort" functions again to format the report correctly, and then finally put it into a new text file titled "suspicious_report.txt". For the irresponsible behavior code, I began by creating a dictionary called "irresponsibleAct", and created a "irresponsibleCount" equalling to 0. Iterations were used to help form expressions for the "loginCount" and "logoutCount". I utilized conditional statements to show if the "loginCount" was greater than the "logoutCount", and if it was, then the "irresponsibleCount" would increase by 1. The "append" and "sort" functions were used again to format the report, and then I put it into a new text file titled "irresponsible_report.txt". For the system glitch code, I began by creating a dictionary called "systemGlitch", and created a "systemGlitchCount" set equal to 0. I utilized iterations to help form expressions for the "logoutCount" and "loginCount". Conditional statements were used to show to correctly format the report, and then I put it into a new text file titled "glitch_report.txt". The system glitch report was the exact opposite to the irresponsible behavior report, and their codes were very similar. Finally, for the domain count report I formed a dictionary titled "domains_dict" and also used the "keys" function to access the list of emails from the log file. I used iterations to show where the "split" was in the email, separating the name and domain name. The symbol separating these two was the "@" sign. After that, I used condtional statements to show that if the domain was in domains_dict, then it would increase by 1. If the domain was not in domains_dict, then it would just equal to 1. I then formatted the report further, and finally closed the file.
