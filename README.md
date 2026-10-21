# Cisco Packet Tracer Email Server Lab

Cisco Packet Tracer lab demonstrating a small LAN email service with client mail configuration and message retrieval.

## Project Overview

This project documents a small local-area network (LAN) configured to demonstrate email exchange between Packet Tracer PCs and an email server. The supplied screenshots show a server connected through a switch, client PCs using the `192.168.10.0/24` network, and successful mail retrieval in the Packet Tracer Mail Browser.

## Features

- Small switched LAN with two client PCs and an email server
- Example host addressing in the `192.168.10.0/24` subnet
- Email client configuration and inbox/message-view evidence
- Screenshots documenting the topology and successful mail retrieval shown in the supplied images

## Technologies Used

- Cisco Packet Tracer
- Ethernet LAN
- IPv4 addressing
- Email services (SMTP/POP3 concepts)

## Project Structure

```text
packet-tracer-email-server-lab/
├── README.md
└── screenshots/
    └── [project screenshots]
```

## Network Topology Details

The screenshots show a 2960-series switch connecting two PCs and a server. Visible example addresses include server `192.168.10.1`, PC0 `192.168.10.2`, and PC1 `192.168.10.3`. The images show email messages in a client inbox and a successful POP3 receive status. Exact interface assignments and all service settings are not fully readable in every screenshot, so use the original Packet Tracer file or your own configuration as the source of truth.

## How to Recreate and Test

1. In Cisco Packet Tracer, add one 2960 switch, two PCs, and one Server-PT device.
2. Connect each endpoint to the switch using copper straight-through links.
3. Assign unique IPv4 addresses in the same subnet, for example:
   - Server: `192.168.10.1/24`
   - PC0: `192.168.10.2/24`
   - PC1: `192.168.10.3/24`
4. On the server, enable and configure the available email services. Set a domain and create mail user accounts.
5. On each PC, open **Desktop → Email** (or Mail Browser), configure the user's email address, incoming/outgoing server address, username, and password to match the server.
6. Send a message from one client to the other, then use **Receive** on the destination client.
7. Save your Packet Tracer work as a `.pkt` file locally if you recreate the lab.

## Useful Verification Commands

```text
# From a PC Command Prompt
ipconfig
ping 192.168.10.1
ping 192.168.10.2
ping 192.168.10.3
```

## Expected Results

- Client PCs can reach the server and each other if addressing and cabling are correct.
- The email client can send and retrieve messages when account details and server services match.
- The supplied screenshots show messages in the Mail Browser and a “Receive Mail Success” status; this package itself does not include or test a `.pkt` file.

## Screenshots

![Email Topology And Mailbox](screenshots/email-topology-and-mailbox.jpg)
![Email Client Inbox](screenshots/email-client-inbox.jpg)
![Email Server Topology And Mail Test](screenshots/email-server-topology-and-mail-test.jpg)

## Important Notes

- The original `.pkt` file was not provided. This repository contains documentation and screenshots only; it does not contain a reconstructed or tested Packet Tracer project file.
- Screenshots are evidence of the displayed state, not a guarantee that every configuration can be recovered from the images.
- Use non-sensitive demo credentials for a recreated lab.

## Portfolio Use

This project is suitable as a networking lab documentation sample for a student portfolio. Before presenting it as a completed practical implementation, recreate the topology in Cisco Packet Tracer, verify the configuration, and add the resulting `.pkt` file and your own test evidence.
