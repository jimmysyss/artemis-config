This is my testing note on Artemis 
==================================

1. Create 2 brokers with port offset
artemis create mybroker1 --port-offset 0
artemis create mybroker2 --port-offset 0

2. Testing the producer and consumer
./artemis producer --url tcp://localhost:61616
./artemis consumer --url tcp://localhost:61616

3. Enabled clustered
See jgroup.xml and broker.xml <broadcast-groups>, <discovery-groups> and <cluster-connections>

4. Load balancing
See broker.xml, Add <redistribution-delay> in <address-setting> 

5. Enable SSL for HornetQ OpenWire protocol
a. Provide keystore.jks and truststore.jks
b. Config the acceptor in broker.xml