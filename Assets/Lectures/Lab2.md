# 20CYS402 - Distributed Systems and Cloud Computing
![](https://img.shields.io/badge/Batch-21CYS-lightgreen) ![](https://img.shields.io/badge/UG-blue) ![](https://img.shields.io/badge/Subject-DSCC-blue) <br/>
![](https://img.shields.io/badge/Lecture-2-orange) ![](https://img.shields.io/badge/Practical-3-orange) ![](https://img.shields.io/badge/Credits-3-orange) <br/>

## Network Time Protocol (NTP) and Cristian's Algorithm Lab

### Lab Question 1: Implementing NTP Synchronization

**Objective:**
Implement a program to synchronize the local clock of a client with a reference clock using the Network Time Protocol (NTP). Calculate the time offset and round-trip delay.

**Requirements:**
1. Create a server that acts as the reference clock.
2. Create a client that requests the current time from the server.
3. Calculate the time offset (θ) and round-trip delay (δ) using the formulas:
   - Time Offset θ = \(\frac{(T2 - T1) + (T3 - T4)}{2}\)
   - Round-Trip Delay δ = \((T4 - T1) - (T3 - T2)\)
4. Adjust the client's local clock time using the calculated time offset.

**Steps:**
1. Server waits for a time request from the client.
2. Client sends a request to the server at time \(T1\).
3. Server receives the request and records the reception time \(T2\), then sends the current server time \(T3\) back to the client.
4. Client receives the server's response at time \(T4\).
5. Client calculates θ and δ, and adjusts its local clock to \(T4 + θ\).

**Deliverables:**
- Source code for the server and client.
- Demonstration of the client's clock before and after synchronization.
- Explanation of the results and how the synchronization improved clock accuracy.

### Lab Question 2: Cristian's Algorithm for Clock Synchronization

**Objective:**
Implement a program to synchronize the client's clock with the server's clock using Cristian's algorithm.

**Requirements:**
1. Create a server that provides the current time.
2. Create a client that requests the current time from the server and synchronizes its clock.
3. Calculate the estimated server time at the client using the formula:
   - \(T_{\text{Client}} = T_{\text{Server}} + \frac{(T2 - T1)}{2}\)

**Steps:**
1. Server waits for a time request from the client.
2. Client sends a request to the server at time \(T1\).
3. Server receives the request, records the reception time \(T2\), and sends the current server time \(T_{\text{Server}}\) back to the client.
4. Client receives the server's response at time \(T3\).
5. Client estimates the server's time and adjusts its local clock to \(T_{\text{Client}}\).

**Deliverables:**
- Source code for the server and client.
- Demonstration of the client's clock before and after synchronization.
- Explanation of the results and the accuracy achieved with Cristian's algorithm.
