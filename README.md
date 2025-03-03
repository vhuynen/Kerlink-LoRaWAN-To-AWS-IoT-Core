

This guide provides detailed instructions on how to convert an HNT Kerlink Gateway into a private LoRaWAN Gateway and connect it to AWS IoT Core for LoRaWAN.

In the first part, you will learn how to convert your HNT Kerlink Gateway into a private LoRaWAN Gateway and establish a connection between your newly converted gateway and AWS IoT Core.

The second part of this guide explains how to attach your LoRaWAN device to AWS IoT Core **LNS** (**L**oRaWAN **N**etwork **S**erver) and forward the payload message to an MQTT Bridge. It also covers how a Node-Red flow is used to decode the message and how to forward the decoded message to Home Assistant via an MQTT Topic, enabling the ingestion of the JSON payload into MQTT Sensor entities.    

## Architecture Schema
![architecture-Lorawan-gateway_aws-iot-core](./docs/img/Architecture.png)

- [Architecture Schema](#architecture-schema)
- [How to Convert an HNT Kerlink Gateway into a Simple LoRaWAN Gateway](#how-to-convert-an-hnt-kerlink-gateway-into-a-simple-lorawan-gateway)

## How to Convert an HNT Kerlink Gateway into a Simple LoRaWAN Gateway

