1.
Add images of your choice for the logo and adjust the path to the PNG file. Uncomment and adjust the next lines

line 151	#icon_photo = PhotoImage(file='C:/Users/nikni/Desktop/SXR8_program/logo_48x48.png') add your own photo
line 152	#root.iconphoto(True, icon_photo)

2.
Add your sender email with a password, here is quick guide how you do it:
Go to your Google Account settings.
Select "Security."
Under "How you sign in to Google," choose "2-Step Verification."
At the bottom of the page, select "App passwords."
Enter a name to help you remember where you'll use the app password.
Click on "Generate."
Then, update the following lines:

line 355    posiljatelj = "ENTER EMAIL ADDRESS"
line 356    geslo = "ENTER YOUR EMAIL PASSWORD"

3.
Exclude the folder/exe from Windows Defender to prevent it from being deleted. Here's how you do it:
Open Windows Security and select "Virus & threat protection".
Under Virus & threat protection settings, click on "Manage settings" in the Virus & threat protection settings section.
Scroll down to the Exclusions section and click on "Add or remove exclusions", then select the folder containing the program.

4.
Run pyinstaller in the command prompt in correct depository: (pyinstaller -F -w -i icon.ico main.py) -> for a program with an icon.
The icon file needs to be in ICO format and in the same folder as the .py file.



Program's Purpose:
This program is designed to retrieve the current price of index SXR8 from the web and send an email to all addresses stored in the database in the event of a significant price drop.
You have the flexibility to set the percentage threshold for the price drop that triggers the email notification.
Additionally, you can configure the frequency at which the program checks the price throughout the day.

The prices of SXR8 will be stored in the database, and the graphical user interface (GUI) will provide insights into the weekly highest and lowest prices.
 Price drops are calculated based on the current price compared to the weekly highest price.

Furthermore, the program allows manipulation of the email database, enabling actions such as adding and deleting email addresses from the database.
