# heartbeatsensor
A sample Azure IoT Edge module that periodically sends simulated deviceID, heartbeat readings and timestamp to Azure IoT Hub.

Install required packages.

    npm install azure-iot-device azure-iot-device-mqtt@latest --save
    npm install node-datetime --save
    npm install minimist --save
    
Replace your device id and connection string in config.json file.

    {
        "deviceId" : "D0001",
        "connectionString" : "HostName=yourhost.azure-devices.net;DeviceId=D0001;SharedAccessKey=yourshareaccesskey"
    }

Now start to program to send the messages to Azure IoT Hub.

    node index.js
You will see the logs as below.

    Connection String:HostName=yourhost.azure-devices.net;DeviceId=D0001;SharedAccessKey=yourshareaccesskey
    Device ID:D0001
    Client connected
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":62.88167688750685,"timestamp":"2018-02-02 01:16:07"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":68.10121876630073,"timestamp":"2018-02-02 01:16:17"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":68.26629231577728,"timestamp":"2018-02-02 01:16:27"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":62.03692698913298,"timestamp":"2018-02-02 01:16:37"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":62.63262499182217,"timestamp":"2018-02-02 01:16:47"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":67.7533426844405,"timestamp":"2018-02-02 01:16:57"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":62.43153752357327,"timestamp":"2018-02-02 01:17:07"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":71.67754257643843,"timestamp":"2018-02-02 01:17:17"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":69.05715105554246,"timestamp":"2018-02-02 01:17:27"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":63.7638946158808,"timestamp":"2018-02-02 01:17:37"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"heartbeat","heartbeat":73.69191754912609,"timestamp":"2018-02-02 01:17:47"}
    send status: MessageEnqueued

     
