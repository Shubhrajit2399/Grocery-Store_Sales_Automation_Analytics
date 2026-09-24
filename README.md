# Grocery-Store_Sales_Automation_Analytics
Motive: We are automating business of a demo Grocery Store which is in both B2B and B2C sales.

Overview: We are making an automated system that will generate files automatically on weekly basis where store-keeper will keep daily sales record. Next we will fetch those files for sales-analytics purpose automatically time-to-time and will send an interpreted analytics report via mail to the business owner for business betterment. 

Obstacle: Our client don't use any formed Database Subscription and also don't want to use any paid membership initially.

##Work:

Step-1:
We are using Google Drive for data storing purposes now. We have created one folder inside our desired drive location. Now we have automated the weekly basis Google Sheet file creation with some pre-defined fixed columns inside this folder.
We have placed one Javascript Code-Snippet inside Google Apps-Script where we linked this Drive folder-path and defined a weekly time-based trigger to create an empty Google-Sheet file on each week Wednesday.

<img width="1423" height="496" alt="Screenshot 2026-09-09 at 8 52 40 AM" src="https://github.com/user-attachments/assets/9aac2b77-d805-4dca-bfb0-857302882105" />

Code is in Code.gs and appscript.json files.

Trigger->

<img width="1429" height="252" alt="Screenshot 2026-09-09 at 9 01 18 AM" src="https://github.com/user-attachments/assets/fab558c6-3019-4724-8ee4-017a403967c2" />


Step-2:
We have created one more Js code-snippet and set it's trigger on each week Tuesday in between 10-11 PM IST. This code will fetch the data from the Drive folder-path files on weekly basis and append data in a Master-File. This code will also format the Date of the source file into a readable form for Analytics Tool.

<img width="1426" height="255" alt="Screenshot 2026-09-16 at 7 11 20 AM" src="https://github.com/user-attachments/assets/993319b4-e359-4111-bf6e-aaeae65843fd" />


Code is in Code.gs_Master-File and appscript.json_Master-File files.

Step-3:
Now throughout the whole week store-keeper inserts sales data inside the file created in Step-1.

Step-4:
We have now designed a report in Google Looker-Studio to plot that data from Master-File.

<img width="1425" height="768" alt="Screenshot 2026-09-11 at 7 45 25 PM" src="https://github.com/user-attachments/assets/3b65af22-f924-428c-8614-4b7b45d8bbb1" />


In the Report Resource tab we have edited the Managed resources on a Data freshness trigger in each 15 minutes. This will update the report resources in 15 minutes when it gets notification of any update on Master-File. So, the Master-File will be updated via App-Script Js code on each Tuesday between 10-11 PM IST and as soon as it updates, after 15 mins the Looker-Studio Data resources will also refresh to get the new data added automatically in the Report.

<img width="1428" height="488" alt="Screenshot 2026-09-12 at 10 17 49 AM" src="https://github.com/user-attachments/assets/0419c68c-e268-4289-b426-03fc45fca360" />

Step-5:
Next we have automated the Looker studio Report delivery option. On each Tuesday 11.30 PM IST the view format of updated report will be sent to the owner mail id automatically. Owner will be able to interact with the report, share and download from the shared link over mail.

<img width="604" height="408" alt="Screenshot 2026-09-14 at 7 42 42 AM" src="https://github.com/user-attachments/assets/6e195398-f2d0-4ed4-9d68-9756a385b186" />

Next we will test this whole automation workflow on scheduled time.

##Result:

Now as per our desired workflow, the automation is generating a report of the weekly sales activities and send a view format of it via mail in the selected mail id's on every Tuesday in between 11.30- 11.45 PM IST.

<img width="1424" height="580" alt="Screenshot 2026-09-16 at 7 17 21 AM" src="https://github.com/user-attachments/assets/ed9d41e8-5cf4-4167-9b16-c4d7724c1ed0" />

The report link is inside the mail and by clicking that it redirects to the interactive window from where customer can view and filter down the sales figures and get a clear knowledge of how profit and sales figures as well low and high performing sales-unit.

<img width="1427" height="765" alt="Screenshot 2026-09-16 at 7 32 59 AM" src="https://github.com/user-attachments/assets/c337b87c-baac-4cca-994f-15377fcf2768" />

The same report can be downloaded in pdf format same-time on-click (sample file attached).

On the next Wednesday a new sheet also gets generated thru the automation and through out the week store-keeper inserts sales data inside it and after a week on next Tuesday the new entries appended in the Master Data Sheet and a consolidated report is sent in mail via automation.

<!--End_of_File--!>
