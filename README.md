A Maimon scan is a network scanning technique that sends a TCP packet with both the FIN and ACK flags set. It's used to find open or filtered ports. 
How it works
The Maimon scan sends a FIN packet, followed by an ACK packet 
The target should respond with an RST packet 
If the port is open, many BSD-derived systems delete the packet 
Nmap takes advantage of this to determine open ports 
Why it's useful 
The Maimon scan is another way to elicit responses from systems that are configured to cloak their presence on the network
It's an alternative to FIN probes, which mimic the first step of the TCP breakdown handshake
How to use it 
To use a Maimon scan with Nmap, use the flag -sM
History 
Uriel Maimon discovered the Maimon scan, which he described in Phrack Magazine issue #49 in November 1996
Nmap included the Maimon scan in a release two issues later
