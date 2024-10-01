# TCP Receiver

This project implements a reliable TCP receiver from scratch, designed to handle byte-stream communication and manage out-of-order segments. The project is broken into three core components: ByteStream, Reassembler, and the final TCP receiver that integrates both.

## Features

1. **ByteStream**: A container for managing the writing and reading of bytes with defined capacity, ensuring bytes are stored and accessed in the correct sequence.
2. **Reassembler**: Responsible for assembling the received byte segments into a contiguous byte stream, even if the segments arrive out of order.
3. **TCP Receiver**: Combines the ByteStream and Reassembler, handles TCP sequence numbers, and sends acknowledgment (ACK) and window size to manage data flow.

## Project Structure

- **ByteStream**: Implements a simple data structure for writing and reading bytes. It handles memory limitations and ensures efficient byte handling.
- **Reassembler**: Assembles TCP segments, keeping track of missing bytes and discarding segments that exceed capacity.
- **TCP Receiver**: Manages the communication with the sender, including handling the sequence number wraparound and generating acknowledgments.
