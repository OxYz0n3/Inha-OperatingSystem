# Server Health Checkup Bash Script

This Bash script is designed to perform a comprehensive health checkup of a server. It checks various aspects of server health, including running processes, CPU utilization, memory utilization, zombie processes, load average, and disk/SAN/NAS utilization. Below is an explanation of each function in the script:

## `check_running_processes()`

This function checks the status of running processes on the server. It performs the following checks:

1. **Processes consuming more than 10% CPU:** Lists the top 5 CPU-consuming processes.

2. **List all running 'java' processes:** Lists all processes with 'java' in their name.

3. **List all running 'http' processes:** Lists all processes with 'http' in their name.

4. **List all running 'mysql' processes:** Lists all processes with 'mysql' in their name.

5. **Total number of running processes:** Counts and displays the total number of running processes.

## `check_cpu_utilization()`

This function checks the CPU utilization of the server. It performs the following checks:

1. **CPU utilization of critical processes:** Lists processes (java, http, mysql) with CPU utilization greater than 10%.

2. **Average CPU load in the last minute:** Displays the average CPU load in the last minute.

3. **CPU info:** Provides information about the server's CPU.

4. **Top 5 CPU-consuming users:** Lists the top 5 CPU-consuming users.

5. **CPU core count:** Displays the number of CPU cores on the server.

## `check_memory_utilization()`

This function checks the memory utilization of the server. It performs the following checks:

1. **Freeing up cache:** Clears file system cache.

2. **Display free memory:** Shows the amount of free memory.

3. **Display swap usage:** Displays information about swap space usage.

4. **Top 5 memory-consuming processes:** Lists the top 5 memory-consuming processes.

5. **Available memory in megabytes:** Displays the available memory in megabytes.

## `check_zombie_processes()`

This function checks for zombie processes on the server. It performs the following checks:

1. **Killing zombie processes:** Attempts to kill zombie processes.

2. **List all zombie processes:** Lists all zombie processes.

3. **Count of zombie processes:** Counts the number of zombie processes.

4. **Parent processes of zombies:** Lists the parent processes of zombie processes.

5. **User owning zombie processes:** Lists the users owning zombie processes.

## `check_load_average()`

This function checks the load average of the server. It performs the following checks:

1. **Current load average:** Displays the current system load average.

2. **Load average of the last 5 minutes:** Displays the load average over the last 5 minutes.

3. **Load average of the last 15 minutes:** Displays the load average over the last 15 minutes.

4. **Number of currently running processes:** Displays the number of currently running processes.

5. **Number of users currently logged in:** Displays the number of users currently logged into the server.

## `check_disk_utilization()`

This function checks the disk, SAN, and NAS utilization of the server. It performs the following checks:

1. **Disk I/O statistics:** Displays disk I/O statistics.

2. **Disk usage:** Displays disk space usage.

3. **Inode usage:** Displays inode (file system structure) usage.

4. **List mounted filesystems:** Lists all mounted filesystems.

5. **Display disk partitions and sizes:** Displays information about disk partitions and their sizes.

## `main()`

The `main()` function is the entry point of the script. It calls all the individual check functions mentioned above to perform a comprehensive health checkup of the server.

## Running the Script

To execute the script, simply run it from the command line. Ensure that it has the necessary permissions to access the required system information.
