## Layer 3 Routing and Load Balancer  
This repo contains two SDN application. One is a routing app, and another is a distributed load balancer application. 

reference: https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford_algorithm  
jdk-version: 7  
floodlight-plus document: https://pages.cs.wisc.edu/~mgliu/floodlight-plus-doc/index.html

- start the floodlight app and SDN application:  

  ```
  java -jar FloodlightWithApps.jar -cf loadbalancer.prop
  ```

- start the mininet topology:

  ``` 
  sudo python2 run_mininet.py [topo-name],[host#]
  i.e. sudo python2 run_mininet.py single,3
  ```

- to view the SDN flow table of a switch

  ``` 
  sudo ovs-ofctl -O OpenFlow13 dump-flows [switch-name]
  i.e. sudo ovs-ofctl -O OpenFlow13 dump-flows s1
  ```

  
