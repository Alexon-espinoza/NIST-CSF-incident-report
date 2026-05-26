# Incident Report Analysis: NIST CSF Application

## Summary
A multimedia company suffered a two-hour Denial of Service (DoS) attack that compromised its internal network. A malicious actor took advantage of an unconfigured firewall to send a flood of incoming ICMP packets (pings), overwhelming the network and causing network services to suddenly stop responding. Normal internal network traffic could not access any resources until the incident management team blocked the incoming ICMP packets.

## Identify
A critical vulnerability was identified in the infrastructure due to an unconfigured firewall that allowed the unrestricted passage of ICMP packets. Additionally, this event highlights the need for regular audits of internal networks, systems, devices, and access privileges to proactively identify potential security gaps before they can be exploited.

## Protect
To mitigate future threats and safeguard internal assets, the network security team implemented specific policies and technical tools: a new firewall rule to limit the rate of incoming ICMP packets, and source IP address verification on the firewall to check for spoofed IP addresses in incoming ICMP packets.

## Detect
To increase the speed and efficiency of identifying suspicious activity, monitoring capabilities were enhanced by deploying network monitoring software to detect anomalous traffic patterns. An IDS/IPS system was also integrated to filter out ICMP traffic based on suspicious characteristics.

## Respond
During the event, the incident management team acted to contain and neutralize the DoS attack by blocking incoming ICMP packets. Although this initial measure temporarily took all non-critical network services offline, it effectively stopped the flood of data and isolated the issue.

## Recover
After containing the ping flood and applying the new firewall rules and filters, critical network services were restored. Access to internal resources was fully normalized once the network was no longer saturated, resolving the incident within a two-hour window.

## Reflections/Notes
This incident demonstrates the importance of keeping firewall rules strictly configured under the principle of least privilege (such as limiting or blocking unnecessary ICMP traffic by default). Combining proactive detection tools (IDS/IPS and monitoring) with robust filtering rules will drastically reduce the attack surface against similar DoS attempts in the future.
