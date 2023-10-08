# Embedded Flows for Axis Devices
Application flows to be imported into Node-RED running [Node-RED Installer](https://pandosme.github.io/acap/node-red/2023/09/12/nodered-acap.html) in Axis Cameras.  

## Path Flow Heatmap MongoDB
An application that stores detected objects paths to a MongoDB.  The typical use cases are:
* Flow Heatmap
* Dwell Heatmap
* Forensic search
* Counting

Your application (whatever that may be) queires and process the data from the database.

### Prerequisite
* Axis Camera
* [Node-RED Installer ACAP](https://pandosme.github.io/acap/node-red/2023/09/12/nodered-acap.html)
* Access to a MongoDB. This can easily be installed using docker with the following [docker-compose.yaml](https://github.com/pandosme/EmbeddedFlows/raw/main/resources/mongodb/docker-compose.yaml)

### Installation
Assumed that have the prerequisite...
* Import the [MongoDB Node](node-red-node-mongodb) into Node-RED via Menu | Manage Palette
* Copy [Path Flow Heatmap MongoDB](https://github.com/pandosme/EmbeddedFlows/raw/main/flows/Path%20Heatmap%20MongoDB.json) and import the flow via Menu | Import.
* Configure the MongoDB nodes to point to your MongoDB
* Deploy and go to the Node-RED Dashboard http://camera-ip:1880/ui
    
### Dashboard
The Node-RED dashboard is merly for configuration and validation.  It queries the database and visulize a flow heatmep. Use the settings to ignore unwanted detections.  
![dashboard](/images/dashboard_path_heatmap.jpg)

### Flows
You will need to adjust the flow.  Double-click on one of the brown MongoDB nodes and configure the address to your MongoDB.  Also, double-click the "Authentication Node" at the bottom of the Initiialization Group and set your cameras user and password.

![dashboard](/images/flow_path_heatmap.jpg)

