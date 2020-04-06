This app is designed to help people manage how much they go outside to buy essential items by alerting them of when these items are in stock. People are able to sign up for text notifications on the items that they want to be alerted about. Companies that sell these items can then send out notifications letting people know when they have refilled their stock, stopping people from having to constantly travel and guess which stores have which items.

The app has extensive use of the Twilio API in order to send and recieve text messages. The GUI is designed using Python and Tkinter, which allows stores to easily input which goods they have in stock.
The running of this requires the use of ngrok by @inconshreveable, as a server to take in the data recieved from phone texts. 
The running of this app consists of a few steps:
1. Have python3
2. Have ngrok installed. 
3. Make an account with Twilio (premium account, not trial, strongly reccomended)
4. These are the things that are imported: twilio, tkinter, flask, PIL (pillow). Pip is reccomended for installation if necessary
5. Run command in the directory with the python file and ngrok installation (on UNIX): /ngrok http 5000
- if this fails, run command: sudo lsof -i:5000, and kill the process that appears with command: kill PID
6. Go to the console in Twilio, and see the phone number settings, then copy the first Forwarding address, looks like http://xxxxxxx.ngrok.io, under "a new message comes in"
7. Don't forget to fill in the correct Account SID and Auth Token from the twilio.com/console page. 
8. The app should run with python product2.py. (May need to be python3)
