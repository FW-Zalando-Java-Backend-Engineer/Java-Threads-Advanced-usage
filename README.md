# 🧵 Java Threads – Day 41: Advanced Concepts Recap

Welcome to **Day 41** of our Java Backend Bootcamp! Today we went beyond basic threads and tackled **advanced multithreading** using real-world scenarios. This README serves as your go-to recap for reviewing concepts, accessing live coding demos, assignments, and references.

---

## 📌 What We Covered Today

### ✅ Topics

| Concept                | What?                                                            | Why?                                                                 | How?                                                                                   |
|------------------------|------------------------------------------------------------------|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Thread Synchronization | Ensures exclusive access to shared resources                    | Prevents race conditions and data inconsistency                      | Using `synchronized` keyword on methods or blocks                                      |
| ExecutorService        | A framework to manage thread execution                          | More efficient than creating threads manually                        | Use `Executors.newFixedThreadPool()`, submit `Runnable` or `Callable` tasks            |
| Callable & Future      | Interfaces for asynchronous tasks that return results           | Enables retrieving results from threads                              | Submit `Callable`, retrieve result via `Future.get()`                                  |
| Deadlock Prevention    | Avoid locking issues when multiple threads try shared resources | Critical for systems like banking, ticketing, etc.                   | Lock objects in a consistent order (e.g., by account ID)                               |

---

## 💡 Live Coding Project: Bank Account Transfer System

We simulated a **banking scenario** with two accounts transferring funds concurrently using threads.

- Each `TransferTask` is submitted to an `ExecutorService`
- We used `Callable` to return success/failure from each task
- Used synchronized blocks to ensure safe access to account balances
- Demonstrated deadlock avoidance by ordering locks

---

## 🧪 Practice Exercises

📎 **Exercises GitHub Repo**  
Includes:
- Concurrent tasks simulation
- Shared resource locking with `synchronized`
- Callable and Future task handling


👉 [🍽️ Assignment: Restaurant Order Processing System](https://github.com/FW-Zalando-Java-Backend-Engineer/Restaurant-Order-Processing-System)

---

## 💻 Live Coding Demo

📎 **GitHub Repo – Live Code (Bank Transfer System)**  
👉 [Bank Account Transfer System](https://github.com/FW-Zalando-Java-Backend-Engineer/bank_account_transfer_system)

---

## 🎥 Zoom Recording

📽️ **Zoom Recording – Day 41 Session**  
👉 [INSERT ZOOM RECORDING LINK HERE]

---

## 📂 Live Boards

🧠 **Visual Aids and Collaborative Boards**
- [Deadlock Situation ](https://miro.medium.com/v2/1*pFiainbHT7SfJfEd8wBSyg.png)


---

## 🧠 Concepts to Remember

| Term              | Description                                                                            |
|-------------------|----------------------------------------------------------------------------------------|
| `synchronized`    | Keyword to lock a resource for exclusive access                                        |
| `ExecutorService` | Java utility to manage thread pools                                                    |
| `Callable`        | Similar to Runnable, but returns a value and may throw an exception                    |
| `Future`          | Represents the result of an asynchronous computation                                   |
| `join()`          | Waits for the thread to finish                                                         |
| `get()` (Future)  | Blocks until result is available or times out                                          |
| Deadlock          | Situation where threads wait indefinitely for each other’s locks                       |

---

## 📚 References & Further Reading

- [Java ExecutorService – Baeldung](https://www.baeldung.com/java-executor-service)
- [Java Callable and Future – Baeldung](https://www.baeldung.com/java-callable-future)
- [Synchronized Keyword – Oracle Docs](https://docs.oracle.com/javase/tutorial/essential/concurrency/locksync.html)
- [Avoiding Deadlocks – GeeksforGeeks](https://www.geeksforgeeks.org/deadlock-in-java-multithreading/)
- [Java Threads – Official JavaDoc](https://docs.oracle.com/javase/8/docs/api/java/lang/Thread.html)




