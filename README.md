# Bitdefender's Matter IoT Dataset

This dataset is published exclusively to support lawful cybersecurity, networking, and scientific
research, including the analysis of traffic characteristics, communication patterns, statistical
outliers, anomalous behaviors in communications between Matter IoT devices. The data are provided in
a privacy-preserving form and may be used solely for defensive, analytical, educational, and
public-interest purposes that comply with applicable data-protection, cybersecurity, and ethical
requirements, and must not be used to identify individuals or reconstruct private communications.
Any use for any other purpose is prohibited.

The data have been collected and processed in accordance with applicable data-protection
legislation, including the principles of lawfulness, fairness, transparency, purpose limitation,
data minimization, and security. The dataset does not contain personal data as defined in applicable
law. Where relevant, the information has been anonymized or aggregated to prevent re-identification.

The dataset is released under the [CC BY-NC 4.0 license](https://creativecommons.org/licenses/by-nc/4.0/).

The dataset comprises Matter/Wi-Fi as well as Matter/Thread traffic features captured over a period
of approximately 4 weeks in a realistic (office) environment. The setup has been documented as part
of the BlackHat EU 2025 presentation titled
"[Ghosts in the Stream: Exposing Lives and Devices Behind
Encrypted Doors](https://blackhat.com/eu-25/briefings/schedule/#ghosts-in-the-stream-exposing-lives-and-devices-behind-encrypted-doors-48973)".

The dataset is structured across 5 Comma Separated Values (CSV) files, entitled
`matter_capture_[1-5].csv`. These contain traffic captures collected at different time periods
from various devices. Details on devices, identifiers and wireless communication protocol are
available in `devices.csv`.

The dataset files are provided in compressed format. To decompress all files, run the following
command:

    $ unxz -k matter_capture_*.csv.xz

## Capture file: matter_capture_1.csv

Time interval:

* 2025-09-02 - 2025-09-09
* 2025-10-20 - 2025-10-21 (for AL1 and TR)

Devices involved in this capture:

AL1, ASL, EDW1, EDW2, EMS1, EMS2, ESP, EW, MSP1, MSP2, NL1, NL2, SSP1, SSP2, TR, TSP1, TSP2

Active automations as configured in Home Assistant:

* Automation 1:
  * Trigger: EDW1 opened
  * Actions:  turn on NL1, change it's color to yellow and brightness to 90%
* Automation 2:
  * Trigger: EDW1 closed
  * Actions: turn on NL1, change it's color to magenta and brightness to 65%
* Automation 3:
  * Trigger: 16:00
  * Actions: turn off all devices, close ASL
* Automation 4:
  * Trigger: 19:00
  * Actions: turn off all devices, close ASL
* Automation 5:
  * Trigger: EDW2 opened
  * Actions: turn on NL2, change it's color to green and brightness to 100%
* Automation 6:
  * Trigger: EDW2 closed
  * Actions: turn on NL2, change it's color to red and brightness to 100%
* Automation 7:
  * Trigger: EMS1 detected no motion for 5 minutes
  * Actions: turn off MSP2 and TSP2
* Automation 8:
  * Trigger: EMS2 detected no motion for 2 minutes
  * Actions: turn off ESP, MSP1 and TSP1
* Automation 9:
  * Trigger: EMS1 became "occupied"
  * Actions: turn on MSP2 and TSP2
* Automation 10:
  * Trigger EMS2 became "occupied"
  * Actions: turn on ESP, MSP1 and TSP1
* Automation 11:
  * Trigger: ASL lock
  * Actions: turn off NL1 and NL2
* Automation 12:
  * Trigger: ASL unlock
  * Actions: turn on NL2, set it's temperature to 2745 and brightness to 61%; turn on NL1, set
    it's temperature to 5785 and brightness to 32%
* Automation 13:
  * Trigger: 07:00
  * Actions: turn on TR
* Automation 14:
  * Trigger: temperature over 22
  * Actions: turn off TR
* Automation 15:
  * Trigger: 21:00
  * Actions: turn on AL1
* Automation 16:
  * Trigger: sunrise
  * Actions: turn off AL1

## Capture file: matter_capture_2.csv

Time interval:

* 2025-09-25 - 2025-09-29
* 2025-10-20 - 2025-10-21 (for AL1 and TR)

Devices involved in this capture:

AL1, AMS, ASL, CL, EDW1, EDW2, EMS1, EMS2, ESP, EW, MMS, MSP1, MSP2, NL2, NL3, SSP1, SSP2, TL, TR,
TSP1, TSP2

Active automations as configured in Home Assistant:

* Automation 1:
  * Trigger: 16:00
  * Actions: turn off all devices, close ASL
* Automation 2:
  * Trigger: 19:00
  * Actions: turn off all devices, close ASL
* Automation 3:
  * Trigger: EDW2 opened
  * Actions: turn on NL2 and CL, change their color to green and brightness to 100%
* Automation 4:
  * Trigger: EDW2 closed
  * Actions: turn on NL2 and CL, change their color to red and brightness to 100%
* Automation 5:
  * Trigger: EMS1 detected no motion for 5 minutes
  * Actions: turn off MSP2, TSP2, SSP1 and SSP2
* Automation 6:
  * Trigger: EMS1 detected no motion for 1 minute
  * Actions: turn off NL3
* Automation 7:
  * Trigger: EMS2 detected no motion for 2 minutes
  * Actions: turn off ESP, MSP1 and TSP1
* Automation 8:
  * Trigger: EMS1 became "occupied"
  * Actions: turn on MSP2, TSP2, SSP1, SSP2 and NL3
* Automation 9:
  * Trigger: EMS2 became "occupied"
  * Actions: turn on ESP, MSP1 and TSP1
* Automation 10:
  * Trigger: ASL lock
  * Actions: turn off NL2
* Automation 11:
  * Trigger: ASL unlock
  * Actions: turn on NL2, set it's temperature to 2745 and brightness to 61%
* Automation 12:
  * Trigger: AMS detected no motion for 30 seconds
  * Actions: turn on TL and set it's color to blue
* Automation 13:
  * Trigger: AMS became "occupied"
  * Actions: turn on TL and set it's color to orange
* Automation 14:
  * Trigger: MMS became "occupied"
  * Actions: turn on TL
* Automation 15:
  * Trigger: MMS detected no motion for 30 seconds
  * Actions: turn off TL
* Automation 16:
  * Trigger: 07:00
  * Actions: turn on TR
* Automation 17:
  * Trigger: temperature over 22
  * Actions: turn off TR
* Automation 18:
  * Trigger: 21:00
  * Actions: turn on AL1
* Automation 19:
  * Trigger: sunrise
  * Actions: turn off AL1

## Capture file: matter_capture_3.csv

Time interval:

* 2025-10-08 - 2025-10-13

Devices involved in this capture:

AL1, AL2, AMS, ASL, CL, EDW1, EDW2, EMS1, EMS2, ESP, EW, MMS, MSP1, MSP2, NL1, NL2, NL3, TR, TSP1,
TSP2, SSP1, SSP2

Active automations as configured in Home Assistant:

* Automation 1:
  * Trigger: EDW1 opened
  * Actions: turn on NL1, change it's color to yellow and brightness to 90%
* Automation 2:
  * Trigger: EDW1 closed
  * Actions: turn on NL1, change it's color to magenta and brightness to 65%
* Automation 3:
  * Trigger: 07:00
  * Actions: turn on TR
* Automation 4:
  * Trigger: 12:00
  * Actions: close ASL
* Automation 5:
  * Trigger: 13:00
  * Actions: open ASL
* Automation 6:
  * Trigger: 16:00
  * Actions turn off all devices, close ASL
* Automation 7:
  * Trigger: 19:00
  * Actions: turn off all devices, close ASL
* Automation 8:
  * Trigger: 21:00
  * Actions: turn on AL1 and AL2
* Automation 9:
  * Trigger: EDW2 opened
  * Actions: turn on NL2 and CL, change their color to green and brightness to 29%
* Automation 10:
  * Trigger: EDW2 closed
  * Actions: turn on NL2 and CL, change their color to red and brightness to 15%
* Automation 11:
  * Trigger: EMS1 detected no motion for 5 minutes
  * Actions: turn off MSP2, TSP2, SSP1 and SSP2
* Automation 12:
  * Trigger: EMS1 detected no motion for 1 minutes
  * Actions: turn off NL3
* Automation 13:
  * Trigger: EMS2 detected no motion for 2 minutes
  * Actions: turn off ESP, MSP1 and TSP1
* Automation 14:
  * Trigger EMS1 became "occupied"
  * Actions: turn on MSP2, TSP2, SSP1, SSP2 and NL3
* Automation 15:
  * Trigger: EMS2 became "occupied"
  * Actions: turn on ESP, MSP1 and TSP1
* Automation 16:
  * Trigger: ASL lock
  * Actions: turn off NL1 and NL2
* Automation 17:
  * Trigger: ASL unlock
  * Actions: turn on NL2 set it's temperature to 2745 and brightness: 61%; turn on NL1. set it's
    temperature to 5785 and brightness: 32%
* Automation 18:
  * Trigger: sunrise
  * Actions: turn off AL1 and AL2, open ASL
* Automation 19:
  * Trigger: temperature over 22
  * Actions: TR turn off

## Capture file: matter_capture_4.csv

Time interval:

* 2025-10-13 - 2025-10-20

Devices involved in this capture: the same as `matter_capture_3.csv`

Active automations as configured in Home Assistant: the same as `matter_capture_3.csv`

## Capture file: matter_capture_5.csv

Time interval:

* 2025-10-23 - 2025-10-27

Devices involved in this capture: the same as `matter_capture_3.csv`

Active automations as configured in Home Assistant: the same as `matter_capture_3.csv`

## Description of the fields

Following, is a description of the fields found in each dataset file:

* timestamp (seconds.microseconds): PCAP capture epoch arrival time
* packet_len (integer): packet length, including all headers and payload
* src_id (integer): device identifier for the source that issued the packet
* dst_id (integer): device identifier for the destination of the packet
* ip_tos (integer): IPv4 header type of service
* ip_id (integer): IPv4 header identification
* ip_flags (integer): IPv4 header flags
* ip_frag (integer): IPv4 header fragmented offset
* ip_ttl (integer): IPv4 header time to live
* ip_proto (integer): IPv4 header next level protocol
* ip_src (string): IPv4 header source address
* ip_dst (string): IPv4 header destination address
* ip6_tc (integer): IPv6 header traffic class
* ip6_fl (integer): IPv6 header flow label
* ip6_nh (integer): IPv6 header next header
* ip6_hlim (integer): IPv6 header hop limit
* udp_sport (integer): UDP header source port value
* udp_dport (integer): UDP header destination port value
* matter_len (integer): length of the Matter header+payload
* matter_message_flags (integer): Matter header message flags
* matter_session_id (integer): Matter header session ID
* matter_security_flags (integer): Matter header security flags
* matter_message_counter (integer): Matter header message counter
* matter_source_node_id (integer): Matter header source node ID
* matter_destination_node_id (integer): Matter header destination node ID
* matter_has_encrypted_payload (boolean): flag indicating if the Matter Protocol Header is encrypted
* matter_enc_payload_len (integer): the length of the encrypted payload following the Matter header
* matter_exchange_flags (integer): Matter Protocol Header exchange flags
* matter_protocol_opcode (integer): Matter Protocol Header protocol opcode
* matter_exchange_id (integer): Matter Protocol Header exchange ID
* matter_protocol_id (integer): Matter Protocol Header protocol ID
* matter_ack_msg_counter (integer): Matter Protocol Header acknowledged message counter

Some fields that are typically found in network protocols have been purposefully excluded for
privacy reasons. The excluded fields are the following:

* Ethernet MAC addresses
* Ethernet type field
* IPv4 version field
* IPv4 header length
* IPv4 total length
* IPv6 version field
* IPv6 payload length
* IPv4 checksum
* IPv6 addresses
* UDP checksum
* UDP length
* Matter Header integrity check
* Matter Protocol Header vendor ID
