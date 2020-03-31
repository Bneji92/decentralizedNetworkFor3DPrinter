# decentralizedNetworkFor3DPrinter
decentralizedNetworkFor3DPrinter

This is the prototype of the decentralized network for 3D printer. 

The following is a short explanation of the components.

3D CLient : Is the backend component of the 3D printer of this network and can be either linked
directly to a printer or set up as mock up for show cases. Either way the functionality doesn't change,
the only difference is that a mock up will log an error because it cannot connect to the printer.
IMPORTANT: Look for manger url in the config and change it to the url of the destination where you placed the manager.
FRAMEWORK: Node.js

clientUi: Is the frontend component of the 3D printer of the network. It sets up th configuration of the printer and gives
visual feedback about the status of the printer. 
IMPORTANT: Look for client url and change it to the url of the destination where the 3D CLient component is deployed.
FRAMEWORK: Angular

Manager: Is the backend component of the network. Handles all incoming offers and orders, declares a winning printer for each
order. It also handles linking between user giving order and printer receiving the order for payment. Manager can be deployed anywhere,
for the case of this prototype it was deployed on a raspberry pi 3.
FRAMEWORK: Node.js

frontend: Is the frontend component of the network. It is the graphical interface for the user to upload orders. The frontend is 
directly connected to the manager and used for visual feedback to the use about the status of the order.
FRAMEWORK: Angular 

WalletForPrinter: Is an other backend component of the printer. This component is linked to the obyte platform (crypto recurrence) with which the payment for the
order and the service is realized. Holds the wallet and the crypto currency for the printer.
IMPORTANT: For payment the obyte app is mandatory, because it is realized through qrcode scanning which is made possible through the app.
FRAMEWORK: Node.js
