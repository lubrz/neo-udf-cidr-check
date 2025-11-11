# User Defined Function for Neo4j to verify if an IP address belongs to a specific network

This is a project I have created while learning more about Neo4j User Defined Functions (UDF).

For this project I have created a UDF which allows the user to check if a Node property ipAddress belongs to a specific network.

## Example

In my Neo4j database we have a number of Nodes which represent servers with a property `ip`


![MATCH Nodes with label Server][img/match_servers.png]


We can see the IP addresses by displaying the output in a table

![MATCH Nodes with label Server - Table][img/match_servers_table.png]

We can then use the **UDF** to match Nodes with label `:Server` which contain `web-server` in the name property and verify if the IP address associated with the node property `ip` belongs to a specific network (in the example we are using `10.10.0.0/16`)

![Use UDF to check if IP address belongs to a Network][img/match_servers_table.png]