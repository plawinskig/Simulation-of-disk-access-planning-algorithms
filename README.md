# Disk Access Planning Algorithms Simulation

This project simulates disk scheduling algorithms and compares their performance. It includes:

- FCFS
- SSTF
- SCAN
- C-SCAN
- EDF
- FD-SCAN

## Project structure

- `src/Main.java` - entry point for the simulation
- `src/Simulation/` - simulation engine, disk model, and request generation
- `src/Schedulers/Algorithms/` - disk scheduling algorithm implementations
- `src/Schedulers/Strategies/` - deadline-aware scheduling strategies
- `src/Comp/` - comparator utilities

## Requirements

- Java JDK installed (Java 8 or newer)

## Build and run

From the repository root, run the following commands in a terminal:

```powershell
javac -d out src/Main.java src/Simulation/*.java src/Schedulers/*.java src/Schedulers/Algorithms/*.java src/Schedulers/Strategies/*.java src/Comp/*.java
java -cp out Main
```

If the build is successful, the simulation will execute and print the results for each algorithm.

## Customizing the simulation

Open `src/Main.java` and update the simulation parameters such as:

- `numberOfRequests`
- `maxArrivalTime`
- `diskSize`
- `maxDeadlineTime`
- `percentOfProcessesWithDeadline`
- `numberOfBehindHeadRequests`
- `numberOfCloseTogetherRequests`
- `centerOfCloseTogetherRequests`
- `radiusOfCloseTogetherRequests`
- `print` array to enable or disable per-algorithm logging

## Notes

- The project uses package declarations for most source files, while `Main.java` is located at the top-level `src/` directory.
- The `out` directory is created by the `javac` command and holds compiled `.class` files.
