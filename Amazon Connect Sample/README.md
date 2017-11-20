# Plantronics Amazon Connect Sample Code
This GitHub repo contains the sample code to illustrate integrating Plantronics with Amazon Connect.

Note: to make this work with YOUR OWN Amazon Connect instance, you need to update the URL in the code where it says: https://your-amazon-connect-domain/ 

### Getting Started with Plantronics Amazon Connect integration sample code
This sample code illustrates how to integrate Plantronics Amazon Connect Contact Control Panel (CCP) with the Plantronics REST API in order to implement headset call control for Amazon Connect.
#### The 4 files that comprise it are:
1. Plantronics Amazon Connect.html
2. amazon-connect-v1.2.0.js
3. spokes.js
4. util.js
#### Screenshot
Here is a screenshot of the sample code in action
![Here is a screenshot of the sample code in action](https://pltdev.github.io/Plantronics%20Amazon%20Connect%20Sample%20Code.png "Here is a screenshot of the sample code in action")
#### List of pre-requisites
* Install Plantronics Hub from: www.plantronics.com/software
* Note Firefox users: If you get "Error connecting to Plantronics Hub." then visit this URL: https://127.0.0.1:32018/Spokes/DeviceServices/Info and click Advanced > Add Exception... to add a security exception to allow the connection.
#### List of features included with this sample code
* CCP (Contact Control Panel) embedded on custom page with JavaScript that connects to Amazon Connect Streams API and Plantronics REST API (client-based API)
* Call control integration with call answer/end controlled by headset button
* Wireless audio link established when on call (required for Plantronics legacy products)
* Agent Availability (Offline/Available) based on headset QD (Quick Disconnect) connector (note, the defined agent states must be Offline/Available - currently hard-coded in this sample code
#### Steps needed to run this sample code:
1. You need to host your copy of these files on your own secure web server (https) on the Internet, e.g. https://your-domain/Plantronics%20Amazon%20Connect.html, and have https://your-domain whitelisted in your Amazon Connect instance, in order to allow the page to embed your CCP (Contact Control Panel). For more info see the “Getting Started, Whitelisting” section of: https://github.com/aws/amazon-connect-streams/blob/master/Documentation.md 
2. In the file "Plantronics Amazon Connect.html" you need to change the **ccpUrl** value to your own Amazon Connect instance (for example https://your-amazon-connect-domain/connect/ccp#/ Note: the Amazon Connect domain will be the same as the domain in the URL you use to administrate your Amazon Connect instance.
3. Load the solution in your web browser, e.g. visit https://your-domain/Plantronics%20Amazon%20Connect.html
#### Troubleshooting
* If your CCP (Contact Control Panel) fails to embed but opens in a seperate Tab, try closing the Tab and reloading the page "https://your-domain/Plantronics%20Amazon%20Connect.html". 
* If it continues to fail to embed you can try logging into CCP one time within seperate Tab, then closing the Tab and reloading page "https://your-domain/Plantronics%20Amazon%20Connect.html".
* If it still continues to fail to open the browser developer tools / inspect element and open go to the Console, then reload the page "https://your-domain/Plantronics%20Amazon%20Connect.html" and look for errors in the Console.