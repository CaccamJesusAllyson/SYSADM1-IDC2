![image](https://github.com/user-attachments/assets/a3ec0a72-84a1-4e48-a733-d5d092fa9121)


# SYSADM1 -- Capacity Management & Planning

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![](vertopal_1f4e6d9df7d14c93bf8a610b3e8a40c4/media/image2.bin){width="5.049483814523184in"
height="3.8229166666666665in"}

**Bottlenecks:**

1.  **Single Firewall**: All VLAN traffic is routed through a single
    firewall, which can create a significant bottleneck during peak
    usage times.

2.  **Layer 2 Switches**: The current Layer 2 switches lack inter-VLAN
    routing capabilities. This limitation forces all inter-VLAN traffic
    to pass through the firewall or a Layer 3 device, which can lead to
    overload.

3.  **Edge Router**: As traffic increases, the edge router may struggle
    to efficiently manage external requests.

**Capacity Limitations:**

1.  **Server Allocation per VLAN:** Each VLAN has a limited number of
    servers. During high-traffic periods, this can hinder the VLAN\'s
    ability to manage increased user requests.

2.  **Bandwidth:** The uplink bandwidth between switches, the firewall,
    and the edge router is insufficient, potentially causing network
    congestion.

**Security Risks:**

1.  **Flat VLAN Structure**: The lack of segmentation beyond VLANs can
    expose sensitive data if one VLAN is compromised.

2.  **Firewall Overload**: Relying on a single firewall creates a point
    of failure that could result in downtime during traffic spikes.

3.  **No Redundancy**: The absence of redundant connections or devices
    could lead to significant downtime if any component fails.

####  **Addressing Bottlenecks**

-   **Upgrade to Layer 3 Switches**: Replace Layer 2 switches with Layer
    3 switches to handle inter-VLAN routing internally, reducing the
    load on the firewall.

-   **Load Balancer Deployment**: Introduce load balancers to distribute
    traffic across multiple servers within VLANs to prevent overloading
    any single server.

-   **High-Capacity Firewall**: Upgrade the firewall to a model with
    higher throughput capacity or deploy multiple firewalls in an
    active-active configuration.

> **Drawbacks**:

-   Increased costs due to hardware upgrades.

-   Complexity in configuring and maintaining load balancers and
    > multiple firewalls.

####  **Improving Scalability**

-   **Bandwidth Upgrades**: Increase the uplink bandwidth between
    switches, the firewall, and the router to accommodate higher traffic
    volumes.

-   **Vertical and Horizontal Server Scaling**:

    -   Vertical Scaling: Add resources (RAM, CPU) to existing servers.

    -   Horizontal Scaling: Add more servers to each VLAN and configure
        clustering for better load distribution.

-   **Cloud Integration**: Use cloud services (e.g., AWS, Azure) to
    handle overflow traffic during peak times.

-   **Redundant Links and Devices**: Implement redundant connections and
    devices to ensure high availability.

> **Drawbacks**:

-   Cost considerations for additional hardware or cloud services.

-   Cloud reliance might introduce latency for some applications.

####  **Enhancing Security**

-   **Segmentation with ACLs**: Apply Access Control Lists (ACLs) and
    policies at Layer 3 switches for stricter inter-VLAN communication
    controls.

-   **Redundant Firewalls**: Deploy a secondary firewall for failover.

-   **DDOS Protection**: Use DDOS mitigation services or appliances to
    protect against traffic surges from attacks.

> **Drawbacks**:

-   Security measures might introduce latency or additional complexity.

-   Firewall redundancy increases hardware costs.

To enhance the network\'s scalability, we should deploy Layer 3 switches
with 10Gbps uplink ports and a next-generation firewall that supports at
least 10 Gbps throughput. Utilizing routers with advanced queuing
mechanisms will help manage traffic spikes effectively. On the software
side, implementing Quality of Service (QoS) will prioritize critical
traffic, while enabling VLAN tagging (802.1Q) will improve organization.
Additionally, using dynamic routing protocols like OSPF or BGP can speed
up routing processes. To reduce server load, a Content Delivery Network
(CDN) can cache static content closer to users. Finally, monitoring
tools like Nagios or SolarWinds should be employed to track network
performance and quickly identify issues.

**Proposed Network Design**

![](vertopal_1f4e6d9df7d14c93bf8a610b3e8a40c4/media/image3.png){width="7.027083333333334in"
height="5.590277777777778in"}

**Evaluating the Plan:**

1.  **Cost:**

> Upgrading hardware is expensive, but it's a good investment for future
> growth.
>
> Cloud services can help save money initially but might add up over
> time.

2.  **Complexity:**

> Managing new devices like load balancers and advanced firewalls will
> require training. Setting up the new system might take some time.

3.  **Impact:**

> These upgrades will make the network faster and more reliable. It'll
> handle more traffic and be more secure against attacks.

  ------------------------------------------------------------------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts
  ----------------- ------------------ ------------------- ---------------------
  **Network         Accurately         Identifies key      Identifies some basic
  Analysis**        identifies         network components  network components
                    potential          and some potential  but lacks a
                    bottlenecks,       bottlenecks.        comprehensive
                    security risks,                        analysis.
                    and capacity                           
                    limitations.                           

  **Scalability     Proposes multiple  Proposes some       Proposes limited
  Planning**        relevant solutions relevant            scalability
                    and provides       scalability         strategies.
                    detailed           strategies but      
                    explanations,      lacks detail.       
                    including                              
                    potential                              
                    drawbacks and                          
                    benefits.                              

  **Evaluation of   Proposes           Provides a basic    Does not evaluate the
  Solutions**       comprehensive      evaluation of the   proposed solutions or
                    scalability        proposed solutions, provides a
                    strategies,        but lacks depth.    superficial
                    including specific                     evaluation.
                    recommendations                        
                    for hardware                           
                    upgrades, software                     
                    configurations,                        
                    and network                            
                    optimizations.                         

  **Proposed        Provides a         Provides a basic    Does not provide a
  Design**          detailed and       design but lacks    clear and detailed
                    well-justified     specific details    design.
                    design, including  and justifications. 
                    network diagrams,                      
                    configuration                          
                    details, and                           
                    implementation                         
                    plans.                                 

  **Evaluation and  Provides a         Provides a basic    Does not evaluate the
  Justification**   thorough           evaluation of the   proposed solutions or
                    evaluation of the  proposed solutions, provides a
                    proposed           but lacks depth.    superficial
                    solutions,                             evaluation
                    considering                            
                    factors like cost,                     
                    complexity, and                        
                    potential impact.                      

  Score:                                                   /50
  ------------------------------------------------------------------------------

References:

GeeksforGeeks, "Inter VLAN routing by Layer 3 switch," *GeeksforGeeks*,
May 02, 2023. Available:
<https://www.geeksforgeeks.org/inter-vlan-routing-layer-3-switch/>

"Inter-VLAN routing: configuration examples." Available:

> <https://www.catchpoint.com/network-admin-guide/inter-vlan-routing>

GeeksforGeeks, "Packet queuing and dropping in routers,"
*GeeksforGeeks*, Jul. 06, 2022. Available:
<https://www.geeksforgeeks.org/packet-queuing-and-dropping-in-routers/>
