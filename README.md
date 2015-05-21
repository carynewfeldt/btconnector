# btconnector

A general test to build a connection to a low power bluetooth device

This write up assumes you have node with NPM installed. If not please install node and NPM on your system.

(NPM install instructions)[https://www.npmjs.com/package/npm]

The js files listed below are example files from the (noble git repository)[https://github.com/sandeepmistry/noble/tree/master/examples]

## Steps

* Clone this project

<pre>$ git clone https://github.com/carynewfeldt/btconnector.git</pre>

* Change in the the btconnector folder

<pre>$ cd btconnector</pre>

* Issue a npm install command

<pre>$ npm install</pre>

* You will see a number of node modules being installed to your system
* Now test the bluetooth connection to the device
* Call the node advertisement-discovery.js file to connect to all bluetooth devices in your vicinity

<pre>

$ node advertisement-discovery.js

hello my local name is:
  Apple TV
can I interest you in any of the following advertised services:
  []
here is my manufacturer data:
  "4c0009060286a9fef46c"

</pre>

* Test connection to a specific device
* In the peripheral-explorer.js add the device UUID to the peripheralUuid variable.
* Ensure your device is in discover mode
* Call the node peripheral-explorer.js file to connect to the specified bluetooth device
* You will see the following if connection is successful

<pre>

$ node peripheral-explorer.js

peripheral with UUID 1c234567cc24acc4c2c2e0e03cfc123 found
  Local Name        = DEVICE_NAME
  TX Power Level    = 3
  Manufacturer Data = ffff12345f
  Service Data      = [object Object]
  Service UUIDs     =
{ localName: 'DEVICE_NAME',
  txPowerLevel: 3,
  manufacturerData: <Buffer ff ff ff ff ff>,
  serviceData: [ { uuid: '180a', data: <Buffer 00 00 00 00 00 00 00 aa 00> } ],
  serviceUuids: [] }
services and characteristics:
180a (Device Information)
  2a29 (Manufacturer Name String) (Manufacturer)
    properties  read
    value       000000000000000000000000000000000000 | ''
  2a24 (Model Number String)
    properties  read
    value       000000000000000000000000000000000000 | 'E\'
  2a25 (Serial Number String)
    properties  read
    value       0000000000000000000000 | ''
  2a27 (Hardware Revision String)
    properties  read
    value       0000000000000000000000 | ''
  2a26 (Firmware Revision String)
    properties  read
    value       0000000000000000000000 | ''
3ea0
  3ea1 (PPG)
    properties  notify
  3ea8 (EDA)
    properties  notify
  3ea3 (ACC)
    properties  notify
  3ea6 (ST)
    properties  notify
3e70
  3e71 (DEVICE command)
    properties  write
3eb0
  3eb2 (DEVICE Control)
    properties  notify
  3eb3 (Battery)
    properties  notify

</pre>
