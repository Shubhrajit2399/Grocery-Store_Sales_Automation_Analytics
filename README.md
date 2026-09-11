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

Code is in Code.gs_Master-File and appscript.json_Master-File files.

Step-3:
Now throughout the whole week store-keeper inserts sales data inside the file created in Step-1.

Step-4:
We have now designed a report in Google Looker-Studio to plot that data from Master-File.

<img width="1425" height="768" alt="Screenshot 2026-09-11 at 7 45 25 PM" src="https://github.com/user-attachments/assets/3b65af22-f924-428c-8614-4b7b45d8bbb1" />
