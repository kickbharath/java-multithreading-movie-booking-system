# 🎬 Movie Ticket Booking System (Java Multithreading)

A simple Java console application built to understand the fundamentals of multithreading, synchronization, and thread safety through a real-world movie ticket booking scenario.

## 📌 Project Overview

This project simulates multiple customers trying to book tickets for the same movie at the same time. Since multiple threads access the same `Movie` object, the application demonstrates how race conditions occur and how they can be prevented using Java synchronization techniques.

The goal of this project was **learning Java concurrency concepts**, not building a complete booking application.

---

## 🚀 Features

* Multiple customers attempting to book tickets simultaneously
* One shared movie object with limited seats
* Thread-safe seat booking using `synchronized`
* Thread creation using `Runnable`
* Waiting for all threads using `Thread.join()`
* Booking history maintained in a repository
* Thread-safe unique Booking ID generation using `AtomicInteger`
* Display of all successful bookings after execution

---

## 🏗️ Project Structure

```text
src
│
├── model
│   ├── Booking.java
│   ├── Customer.java
│   └── Movie.java
│
├── repository
│   └── BookingRepository.java
│
├── service
│   └── BookingService.java
│
├── task
│   └── BookingTask.java
│
└── Controller
    |___Main.java
```

---

## 🧠 Concepts Practiced

* Java Threads
* Runnable Interface
* Shared Resources
* Race Conditions
* Critical Sections
* `synchronized`
* Thread Scheduling
* `Thread.join()`
* Thread Safety
* `AtomicInteger`
* Object-Oriented Design

---

## 🧪 Sample Scenario

* Movie has **5 seats**
* **10 customers** attempt to book simultaneously
* Only **5 bookings succeed**
* Remaining customers receive a "House Full" message
* Every successful booking receives a unique Booking ID

---

## ▶️ How to Run

1. Clone the repository.
2. Open the project in Eclipse, STS, or IntelliJ IDEA.
3. Run the `Main` class.
4. Observe different thread execution orders on each run.

---

## 📚 What I Learned

While building this project, I explored:

* Why race conditions occur
* Why shared mutable state is dangerous
* How `synchronized` prevents multiple threads from modifying shared data simultaneously
* Why thread execution order is unpredictable
* How `Thread.join()` waits for all worker threads to finish
* How `AtomicInteger` can safely generate unique IDs in a concurrent environment
* The importance of designing thread-safe classes

---

## 🔮 Future Improvements

* Use `ExecutorService` instead of manually creating threads
* Implement a Thread Pool
* Return booking confirmations using `Callable` and `Future`
* Add support for multiple movies and multiple screens
* Replace in-memory storage with a database
* Build a REST API using Spring Boot
* Add unit tests

---

## 👨‍💻 Author

**Mitti Bharath**

This project was built as part of my journey to learn Java Backend Development and Java Concurrency from first principles.
