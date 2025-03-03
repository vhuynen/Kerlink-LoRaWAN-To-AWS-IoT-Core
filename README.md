

This guide provides detailed instructions on how to convert an HNT Kerlink Gateway into a private LoRaWAN Gateway and connect it to AWS IoT Core for LoRaWAN.

In the first part, you will learn how to convert your HNT Kerlink Gateway into a private LoRaWAN Gateway and establish a connection between your newly converted gateway and AWS IoT Core.

The second part of this guide explains how to attach your LoRaWAN device to AWS IoT Core **LNS** (**L**oRaWAN **N**etwork **S**erver) and forward the payload message to an MQTT Bridge. It also covers how a Node-Red flow is used to decode the message and how to forward the decoded message to Home Assistant via an MQTT Topic, enabling the ingestion of the JSON payload into MQTT Sensor entities.    

## Architecture Schema
![architecture-Lorawan-gateway_aws-iot-core](./docs/img/Architecture.png)

- [Architecture Schema](#architecture-schema)
- [How to Convert an HNT Kerlink Gateway into a Simple LoRaWAN Gateway](#how-to-convert-an-hnt-kerlink-gateway-into-a-simple-lorawan-gateway)
- [References](#references)

## How to Convert an HNT Kerlink Gateway into a Simple LoRaWAN Gateway

Before starting this project, I contacted Kerlink Support to ask if it is possible to convert an HNT Wirnet iFemtoCell Kerlink Gateway into a simple Gateway. The support team confirmed that it is possible to replace the HNT firmware with standard firmware. I noticed that many HNT gateways are available on the second-hand market, so I bought one for only €80.

A few days later, I received the gateway and started resetting it to factory configuration. I was able to connect to the local console using the admin account and the default password, but I was unable to connect via SSH to the root account. The password did not seem to follow the default format, which is composed of a prefix and the last 6 digits of the serial number, like pdmk-0507DD.

After many hours of reading the support documentation and performing numerous reset operations, I concluded that the gateway had been wiped, but the root account seemed to be restricted to Kerlink support.

Then, I wrote to the support to ask them what the process is to wipe an HNT Gateway to convert it into a simple gateway. The support team informed me that they can activate a magic link to allow the gateway to retrieve a new firmware version from their servers, but this operation is irreversible. Then, I confirmed that I was aware of the irreversibility and that this is what I wanted.

After a latest physical reset button procedure, the gateway finally retrieved the correct firmware version, and it was possible to connect to it with the root account. 

## References

