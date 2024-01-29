
# Shipping Company Management Simulator

-This Data Structures Project simulates a shipping company that delivers cargo using trucks to its customers with modifications to the parameters of the simulation.

-This Simulation includes:
- Regular checkup of trucks after a specefic number of journeys
- Automatric promotion of cargos that have not been loaded for a long time
- Maximum wait time for cargos after which they must be loaded to trucks
- A simulation clock with the format Hours:Days

There are three types of Cargo and trucks:
-
- VIP
- Special
- Normal

-The VIP Cargos can be loaded to any truck (VIP,Special or Normal)

-The Special Cargos can only be loaded to Special Trucks

-The Normal Cargos can only be loaded to VIP or Normal Trucks

-VIP Cargos are loaded first, second are special, and finally normal cargos are loaded last

There are Three types of Events
-

- Ready Event
- Cancellation Event
- Promotion Event

-The Ready Event indicates that a new order for a cargo has arrived

-The Cancellation Event cancels a previous order

-The Promotion Event promotes a package from Normal to VIP
## Input File Format

#Comments start with hashtag such as this one DO NOT INCLUDE THEM IN THE ACTUAL FILE, THESE ARE JUST FOR EXPLANATION

3 3 2 #Number of normal, special, VIP trucks\
80 70 140 #Speed of normal, special, VIP trucks\
3 3 2 #Capacity of normal, special, VIP trucks\
1 9 8 7 # Number of journeys before checkup, Normal, Special, VIP checkup durations\
10 2 # Automoatic Promotion Time, Maximum wait Time\
5 #Number of Events\
R S 1:3 5 500 2 700 # Ready Event, Special Cargo, Arrives Day 1, hour 3, ID 5, Distance of 500, Loading time of 2 hours and a cost of 700\
R V 1:3 6 400 5 1000 # Ready Event, VIP Cargo, Arrives Day 1 hour 3, ID 6, Distance of 400, Loading Time of 5 hours, Cost of 1000\
R N 1:4 7 200 2 500 # Ready Event, Normal Cargo, Arrives Day 1 hour 4, ID 7, Distance of 200, Loading Time of 2 hours, Cost of 500\
X 1:5 6 #Cancellation Event, At Day 1 Hour 5, Of ID 6\
P 1:5 7 600 #Promotion Event, At Day 1 Hour 5, Of ID 7, at new cost of 600

Sample Input File:
-

3 3 2\
80 70 140\
2 3 2\
1 9 8 7\
10 20\
30\
R N 1:0 1 200 2 500\
R N 1:1 2 200 2 500\
R N 1:2 3 250 1 600\
R V 1:2 4 300 2 600\
R S 1:3 5 500 2 700\
R N 1:3 6 400 5 1000\
R S 1:4 7 200 2 500\
X 1:5 2\
P 1:5 3 600\
R N 1:5 8 700 5 1000\
R V 1:6 9 800 3 5000\
R N 1:7 10 900 5 5000\
X 1:8 10\
P 1:8 8 100\
R V 1:8 11 800 2 6000\
R N 1:8 12 800 5 413\
R N 1:9 13 200 2 500\
R S 1:9 14 200 2 500\
P 1:10 12 200\
X 1:10 13\
R N 1:10 15 200 2 500\
R N 1:10 16 50 2 356\
R N 1:11 17 200 2 500\
P 1:12 15 200\
X 1:13 16\
R N 1:15 18 90 3 400\
R V 1:16 19 90 3 500\
X 1:17 18\
R N 1:20 20 56 2 187\
P 1:20 20 560

Sample Output File:
-

CDT	ID	PT	WT	TID\
1:11	3	1:5	0:3	7\
1:14	4	1:5	0:3	7\
1:17	1	1:5	0:7	1\
1:19	16	1:10	0:6	2\
1:20	7	1:5	0:10	4\
1:21	11	1:8	0:5	8\
1:22	14	1:9	0:6	4\
1:23	17	1:11	0:5	2\
2:0	6	1:5	0:7	1\
2:0	9	1:6	0:7	8\
2:1	15	1:10	0:10	3\
2:5	5	1:5	0:10	4\
2:9	20	1:20	0:10	5\
2:12	8	1:5	0:15	3\
2:13	19	1:16	0:14	5\
3:4	12	1:8	0:22	5\
-------------------------------------------------\
-------------------------------------------------\
Cargos: 16 [N: 4, S: 3, V: 9]\
Cargo Avg Wait = 0:8\
Auto-promoted Cargos: 0%\
Trucks: 8 [N: 3, S: 3, V: 2]\
Average Active Time = 16.9271%\
Average Utilization = 16.9271%





## Lessons Learned

- OOP in C++ and Class hierarchy
- How to Debug using VS
- How to implement Data Structures effectively

