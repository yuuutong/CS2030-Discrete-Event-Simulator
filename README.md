# CS2030-Discrete-Event-Simulator
A discrete event simulator is a software that simulates the changes in the state of a system across time, with each
transition from one state of the system to another triggered via an event. Such a system can be used to study many
complex real-world systems such as queuing to order food at a fast-food restaurant.
An event occurs at a particular time, and each event alters the state of the system and may generate more events.
States remain unchanged between two events (hence the term discrete), and this allows the simulator to jump from
the time of one event to another. Some simulation statistics are also typically tracked to measure the performance of
the system.

In this project, we consider a multi-server system comprising the following:
There are a number of servers; each server can serve one customer at a time.
Each customer has a service time (time taken to serve the customer).
When a customer arrives (ARRIVE event):
if the server is idle (not serving any customer), then the server starts serving the customer immediately
(SERVE event).
if the server is serving another customer, then the customer that just arrived waits in the queue (WAIT
event).
if the server is serving one customer with a second customer waiting in the queue, and a third customer
arrives, then this latter customer leaves (LEAVE event). In other words, there is at most one customer
waiting in the queue.
When the server is done serving a customer (DONE event), the server can start serving the customer
waiting at the front of the queue (if any).
If there is no waiting customer, then the server becomes idle again
