# question-no-2071
Solution to the question no 2071 on leet code 

2071. Maximum Number of Tasks You Can Assign
You have n tasks and m workers. Each task has a strength requirement stored in a 0-indexed integer array tasks, with the ith task requiring tasks[i] strength to complete. The strength of each worker is stored in a 0-indexed integer array workers, with the jth worker having workers[j] strength. Each worker can only be assigned to a single task and must have a strength greater than or equal to the task's strength requirement (i.e., workers[j] >= tasks[i]).

Additionally, you have pills magical pills that will increase a worker's strength by strength. You can decide which workers receive the magical pills, however, you may only give each worker at most one magical pill.

Given the 0-indexed integer arrays tasks and workers and the integers pills and strength, return the maximum number of tasks that can be completed.

How it works:
Binary Search is used to find the max number of assignable tasks (mid).

For each guess mid, the check() function tries to assign the hardest mid tasks to the strongest mid workers.

If a worker can't do a task, a pill is used to boost them, if available.

If tasks can be assigned with or without pills, we try a higher mid. If not, we try lower.

Key techniques:
Sorting workers and tasks.

Using a TreeMap to efficiently find the right worker for a task.
