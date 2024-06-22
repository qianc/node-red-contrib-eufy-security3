# TODO List

1. Add method for processing captcha for driver connection

   Eufy Security's api may challenge us with a captcha request for connecting (which is required even if using local/P2P to connect to security devices)

   Currently the response from the api is a captcha ID and base64 encoded image. Bropat's driver can send back the id and resolved captcha to complete the connection process (driver.set_captcha \<captcha\> [\<id\>])

   Primary goal is to detect the event response from the command ("captcha request") and collect the captcha id and image and display it to the nodered dashboard along with a text input and button for collecting the captcha resolve and sending it back for connection.

   It does not appear that the current nodered contrib has a method for this although it will show "awaiting captcha" on the flow editor and store the api's response with id/image in the payload

2. Locate/fix issues with device attributes showing as "undefined" in nodered

   Note that Bropat's implementation of the eufy-security-client with their ioBroker demo, which was also created in nodered, properly returns the values of a device/station's attributes.

3. Use the latest eufy-security-client (currently at 3.0.0)
4. 
