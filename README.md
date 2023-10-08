# EmbeddedFlows
Application flows to be installed for Node-RED running [Node-RED Installer](https://pandosme.github.io/acap/node-red/2023/09/12/nodered-acap.html) in Axis Cameras.  

## Path Flow Heatmap MongoDB
An application that stores detected objects paths to a MongoDB.

### Prerequisite
* Axis Camera
* [Node-RED Installer ACAP](https://pandosme.github.io/acap/node-red/2023/09/12/nodered-acap.html)
* Access to a mongo MongoDB. This can easily be installed using docker with the following docker-compose.yaml

### Dashboard
The dashboard provides a way to visualize detections as a heatmap and also a way to filter unwanted detections.
![dashboard](/images/dashboard_path_heatmap.jpg)

### Flows
![dashboard](/images/flow_path_heatmap.jpg)

