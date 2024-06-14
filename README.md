Process Manager Script
Overview
This Bash script allows users to manage and retrieve information about system processes. Users can choose from three commands: ps, top, and kill. The script displays the output of the selected command.

File Name
program1_process_manager.sh
Author
Kantapong Wongsanguan
Features
Welcome Message: The script starts with a welcome message.
Command Input: Prompts the user to enter one of the following commands: ps, top, or kill.
Decision Structure: Uses if/elif/else to handle different commands.
Error Handling: Displays an error message if the input command is not one of the specified commands.
Usage
Run the script:
bash
Copy code
./program1_process_manager.sh
Enter a command: When prompted, enter ps, top, or kill.
Example Output
bash
Copy code
$ ./program1_process_manager.sh
Welcome to Process Manager
Please enter one of the following commands (ps, top, kill): ps
You have selected ps command
This command displays the processes for the current shell and the output of this command is:
  PID TTY           TIME CMD
35187 ttys000    0:00.11 -bash
46520 ttys000    0:00.00 -bash
Concepts Used
Echo Command: To display messages.
Read Command: To capture user input.
Decision Structures: If/elif/else to handle different commands.
Process Commands: ps, top, kill.
References
Practicals from the CP1409 course.
README for program2_cpu_scheduler.sh
CPU Scheduler Script (First-Come First-Served)
Overview
This Bash script simulates a First-Come First-Served (FCFS) CPU scheduling algorithm. It prompts the user for process descriptions, calculates waiting times, and outputs execution traces.

File Name
program2_cpu_scheduler.sh
Author
Kantapong Wongsanguan
Features
Variable Initialization: Initializes variables for tracking time and waiting times.
Input Handling: Prompts the user for process descriptions (arrival time, burst time) in CSV format.
FCFS Scheduling: Implements FCFS scheduling to calculate and output process execution traces.
Statistics Calculation: Calculates and outputs average waiting time, run time, and other statistics.
Usage
Run the script:
bash
Copy code
./program2_cpu_scheduler.sh
Enter process details: Enter process details in the format arrival time, burst time. Enter a blank line to end input.
Example Output
bash
Copy code
$ ./program2_cpu_scheduler.sh
Enter process details: 0, 2
T: 0, 0, R
T: 1, 0, R
S: 0, 2, 0
Enter process details: 1, 3
T: 1, 1, W
T: 2, 1, R
T: 3, 1, R
T: 4, 1, R
S: 1, 3, 1
Enter process details: 6, 1
T: 5, -, I
T: 6, 2, R
S: 2, 1, 0
Enter process details:
A: 3, 7, 1, 2, .33, 1
Number of processes: 3
Total time / running time / idle time: 7 / 6 / 1
Avg run time / avg wait / longest wait: 2.00 / .33 / 1
Concepts Used
Variable Declaration: To track time and statistics.
Array Declaration: To store waiting times.
Loop Structures: While and for loops to process input and simulate scheduling.
Error Handling: Checks for empty input and incorrect arrival times.
Output Redirection: Uses >&2 for error messages.
References
Lectures and practicals from the CP1409 course.
