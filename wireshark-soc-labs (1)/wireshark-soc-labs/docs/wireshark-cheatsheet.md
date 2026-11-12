# Wireshark cheat sheet

Display filters and features I have used in these labs. Type filters in the green bar under the toolbar.

## Display filters

| Filter | What it shows | Used in |
|--------|---------------|---------|
| `http` | All HTTP requests and responses | Lab 6 |
| `http.request.method == "POST"` | Only HTTP POST requests (where form data is sent) | Lab 6 |
| `ftp.request.command == "PASS"` | FTP password attempts sent by clients | Lab 7 |
| `tcp.analysis.retransmission` | Packets Wireshark flags as retransmitted | Extra |
| `tcp.flags.reset==1` | TCP packets with the RST flag set | Extra |

A filter bar turning **green** means the syntax is valid. Red means it is not.

## Features

| Feature | How to reach it | Purpose |
|---------|-----------------|---------|
| Follow TCP Stream | Right-click a packet, Follow, TCP Stream | Read the full conversation as text. Client data is red, server data is blue. |
| Packet details pane | Click a packet | Expand layers such as *HTML Form URL Encoded* to read fields |
| RTP Player | Telephony menu | Visualise and play back VoIP audio streams |
| Status bar | Bottom of the window | Shows total packets and how many match the filter |

## Habits that save time

- Filter first, then read: narrow thousands of packets down to the few that matter.
- Check the status bar (`Displayed: 25 (6.8%)`) to confirm a filter did what you expected.
- Note the source IP, destination IP, protocol and time for each finding.
