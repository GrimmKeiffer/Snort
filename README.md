# Snort

## Objective
I learned how to use Snort as an open-source intrusion detection and prevention system (IDS/IPS). I gained insights into monitoring network traffic in real time, writing and managing detection rules, and analyzing alerts to identify and respond to potential security threats effectively. Additionally, I developed skills in configuring Snort for specific environments, enabling me to customize its operation to suit various network security needs.

### Skills Learned
- Network traffic analysis
- Rule creation and management
- Intrusion detection and prevention
- Packet analysis
- Log analysis
- Network protocols
- System configuration
- Integration with other tools
- Security threat identification
- Problem-solving and troubleshooting

### Tools Used
- Snort preprocessors
- Snort rules engine
- Snort rule sets
- Snort output plugins
- Snort packet decoder
- Unified output format
- Dynamic modules
- Snort GUI frontends


## Steps
1 ![Snort 1](https://github.com/user-attachments/assets/0074af12-2c1e-46b3-9d69-4399ca9535ba)
- Write a single rule for SNORT traffic
- Detecting traffic on TCP 80

2 ![Snort 2](https://github.com/user-attachments/assets/31a030c9-4b7a-426b-91c4-f1e6f5c9779b)
- after creating the tcp 80 rule on snort I can run our pcap filter
- once I run "sudo snort -A full -r mx-3.pcap c local.rules" I get 328 alerts with 328 logged

3 ![Snort 3](https://github.com/user-attachments/assets/1fac9ed2-861b-4b7c-8a65-ec7767d782b4)
- after the previous run I am able to check packet 63 for the specific details on it in the logs that were created
- specifically I want the destination address for the packet
- the following questions ask for the ACK and  SEQ for packets 62 and 64
- packet 62 and 64 have the same values as 63 so I can gather the information from any of the 3 packets requested

4 ![Snort 4](https://github.com/user-attachments/assets/b69b7412-7cae-42af-b1f1-34f06ceaa3e8)
- the following is asking for the TTL for packet 65 it wasnt much to scroll to find it
- then I need the source IP from packet 65 as well
- additionally I need the source port of the packet as well

5 ![Snort 5](https://github.com/user-attachments/assets/99301537-0393-43e2-9d2b-9c5b46ab85bf)
- Next I made a IDS rul for TCP port 21
- then I needed the number of packets that applied to this ruleset

6 ![Snort 6](https://github.com/user-attachments/assets/53c54c77-58a9-4ddc-a129-62dd2dda4bb3)
- after sorting the log file created with the command "sudo strings snor.log.1688564350 | grep 220 | head"
- I then get the above with successful microsoft FTP service under code 220







