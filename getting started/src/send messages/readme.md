# Send messages

Nunc malesuada volutpat fermentum. Donec in ante nec diam venenatis eleifend. Cras commodo ligula nec justo lacinia fringilla. Morbi eget congue neque. Duis varius eleifend enim eu euismod. Pellentesque scelerisque convallis tortor. Fusce gravida est diam, ac sodales enim consectetur eu. Duis eu consequat massa.

- [Samples](#samples)
- [Installation](#installation)
- [Documentation](#documentation)
- Next Steps

# Samples

### Send messages to IoT Hub
`send_messages.js` `send_messages.ts`

Send messages to IoT Hub using MQTT (default), AMQP, MQTTW (Web Socket), AMQPW (Web Socket), and HTTP
         
[Azure Documentation](https://docs.microsoft.com/en-us/azure/iot-central/core/tutorial-connect-device?pivots=programming-language-javascript) 

### Send messages to IoT Central

Send messages to IoT Central using MQTT (default), AMQP, MQTTW (Web Socket), AMQPW (Web Socket), and HTTP

| JavaScript sample | TypeScript sample |                |
| :---------------- | :---------------- | :------------------ |
| send_messages_iot_central.js  | send_messages_iot_central.ts  | [Create and connect a client application to your Azure IoT Central application](#) |

### Send messages via proxy

Send messages through a proxy

| JavaScript sample |
| :---------------- |
| send_messages_through_proxy.js  |  

### Send messages with x509

Send messages when using an X509 certificate

| JavaScript sample | TypeScript sample |                |
| :---------------- | :---------------- | :------------------ |
| send_messages_with_x509.js  | send_messages_with_x509.ts | [Understanding Public Key Cryptography and X.509 Public Key Infrastructure](https://docs.microsoft.com/en-us/azure/iot-hub/tutorial-x509-introduction) |

### Send messages with SAS token

Send messages with Shared Access Signature (SAS) token

| JavaScript sample | TypeScript sample |                |
| :---------------- | :---------------- | :------------------ |
| send_messages_with_sas.js  | send_messages_with_sas.ts | [Azure Documentation](https://docs.microsoft.com/en-us/azure/iot-hub/tutorial-x509-introduction) |

### Send messages in batch with HTTP

Send several messages in batch using HTTP

| JavaScript sample | TypeScript sample |           
| :---------------- | :---------------- | 
| send_messages_in_batch_http.js  | send_messages_in_batch_http.ts | 

# Installation

## Using GitHub codespaces

You can use Github Codespaces to be up and running quickly! Here are the steps to follow.

**1) Make sure you have the prerequisites**

In order to run the device samples you will first need the following prerequisites:

- An Azure IoT Hub instance. [(Link if you don't.)][https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal]
- A device identity for your device. [(Link if you don't.)][https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal#register-a-new-device-in-the-iot-hub]

**2) Create and open Codespace**

- Select the Codespaces tab and the "New codespace" button
- Once the Codespace is open, all required packages to run the samples will be setup for you

**3) Set the IOTHUB_DEVICE_CONNECTING_STRING environment variable**

- From a shell or Node.js command prompt, navigate to the folder where you placed the sample files.
- Set the `IOTHUB_DEVICE_CONNECTING_STRING` environment variable:

```bash
export IOTHUB_DEVICE_CONNECTING_STRING="<YourIoTHubConnectionString>"
```

**4) Run it**

Run the sample application using the following commands:

_for JavaScript_

```bash
cd device/samples/javascript
node simple_sample_device.js
```

_for TypeScript_

```bash
cd device/samples/typescript/dist
node simple_sample_device.js
```

## Run samples locally

_How to run a sample in your own folder using published npm packages._

**1) Make sure you have the prerequisites**

In order to run the device samples you will first need the following prerequisites:

- The latest or LTS version of Node.js on your device. (Check out [Nodejs.org](https://nodejs.org/) for more info)
- An Azure IoT Hub instance ([Link if you don't](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal))
- A device identity for your device ([Link if you don't](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal#register-a-new-device-in-the-iot-hub))
- Clone this repo to your local machine

**2) Install dependencies**

You need to install proper dependencies as defined in the **package.json**. Run the following commands:

_for JavaScript_

```
cd device/samples/javascript
npm install
```

_for TypeScript_

```
cd device/samples/typescript
npm install
```

**3) Set the IOTHUB_DEVICE_CONNECTING_STRING environment variable**

- From a shell or Node.js command prompt, navigate to the folder where you placed the sample files.
- Set the `IOTHUB_DEVICE_CONNECTION_STRING` environment variable:

_in bash_

```bash
export IOTHUB_DEVICE_CONNECTION_STRING="<YourIoTHubConnectionString>"
```

_in powershell_

```powershell
$env:IOTHUB_DEVICE_CONNECTION_STRING="<YourIoTHubConnectionString>"
```

**4) Build it**

For the TypeScript samples, we need to run the `build` command to transpile the TypeScript code into the JavaScript files:

```
npm run build
```

The JavaScript files are placed into the `dist` folder.

**5) Run it**

Run the sample application using the following commands:

JavaScript

```bash
node sample_sample_device.js
```

TypeScript

```bash
cd dist
node sample_sample_device.js
```
# ➡️Next Steps

- [How to guides](src/../../how%20to%20guides)
- [Solutions](src/../../solutions)
