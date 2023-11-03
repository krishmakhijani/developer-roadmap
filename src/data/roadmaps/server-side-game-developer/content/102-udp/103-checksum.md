# Checksum

The `checksum` is an important element in UDP that ensures the integrity and validation of the data being transmitted. It computes the total sum of all the bytes in a packet and incorporates it as an additional `checksum` field in the UDP header. When the packet arrives at its destination, this process is repeated and compared with the included `checksum`. If a match is observed, the packet is deemed valid. If not, it signifies that an error occurred during transmission possibly due to noise or any third-party interference. In such a case, the packet is simply dropped, as UDP does not initiate any retransmission or error correction procedure. This is why a perfect output cannot be guaranteed with UDP, nor can it determine whether all the recipients are receiving the packets properly.