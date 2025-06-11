# Philosophers

**Philosophers** is a classic concurrency project from the 42 school curriculum, designed to introduce students to multithreading, mutexes, and the challenges of thread synchronization.

## 🧠 Project Overview

The goal of this project is to simulate the famous *Dining Philosophers Problem*, where a number of philosophers sit around a table with a fork between each of them. To eat, a philosopher must pick up both the fork to their left and the fork to their right. They alternate between thinking, eating, and sleeping, but must avoid starving and prevent deadlocks.

Each philosopher is represented by a thread, and forks are managed using mutexes to avoid data races. The simulation must follow strict timing rules and be able to detect when a philosopher dies due to starvation.

The challenge is to coordinate the threads so that philosophers can eat without interfering with each other, ensuring no deadlocks occur and that all timing constraints are respected.

## 🎯 Goals

- Create a simulation using multiple threads (one per philosopher).
- Use mutexes to manage access to forks and avoid race conditions.
- Detect when a philosopher dies (fails to eat within a given time).
- Handle timing accurately for eating, sleeping, and thinking.
- Avoid deadlocks and ensure the simulation can end gracefully.

## 📚 Useful Concepts

- POSIX threads `pthread_create`, `pthread_join`.
- Mutexes `pthread_mutex_lock`, `pthread_mutex_unlock`.
- Time management with `gettimeofday` or `clock_gettime`.
- Avoiding deadlocks and starvation.
- Monitoring threads for death detection.
- Synchronized printing to avoid messy console output.
