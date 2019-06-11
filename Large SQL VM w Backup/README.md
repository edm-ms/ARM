# Multi-Region Virtual Networks With Peering and 2 Subnets Per-Region.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fedm-ms%2Fpoc%2Fmaster%2FMulti-Region-Network%2Ftemplate.json" target="_blank" rel="noopener noreferrer">

<img src="http://azuredeploy.net/deploybutton.png"/>

</a>

<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fedm-ms%2Fpoc%2Fmaster%2FMulti-Region-Network%2Ftemplate.json" target="_blank" rel="noopener noreferrer">

<img src="http://armviz.io/visualizebutton.png"/>

</a>

This template will deploy a virtual network into the following 6 regions:

US East / US West <br>
EU North / EU West <br>
BR South / US South Central <br>

Each of the regions above are Azure "pair" regions allowing for fast failover in the event of a region disaster. More information can be found on paired regions here: <a href="https://docs.microsoft.com/en-us/azure/best-practices-availability-paired-regions" target="_blank"> Azure Paired Regions and BCDR

</a>

The following IP ranges are assigned to each of the virtual networks, but they can be modified in the deployment parameters.

US East -   10.1.0.0/16 <br>
US West -   10.2.0.0/16 <br>
EU North -  10.3.0.0/16 <br>
EU West -   10.4.0.0/16 <br>
BR South -  10.5.0.0/19 <br>
US South Central -  10.6.0.0/19 <br><br>

A Gateway and Management subnet are also created in each region VNET with the following format: <br>

Gateway: x.x.1.0/24 <br>
Management: x.x.2.0/24 <br>