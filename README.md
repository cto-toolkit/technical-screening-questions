# Technical screening questions

ℹ️  This repository contains a number of technical screening questions that can be used when vetting potential candidates

These questions are best used for screening candidates early in your hiring process (to replace/strenghten resume screening and/or HR phone screening). 

🙏  Please open a pull request if you want to add a question or share feedback.


## Backend questions

<details>
<summary>What's the following SQL query is supposed to do?</summary>

```sql
SELECT name, MAX(price) AS price 
FROM articles 
WHERE price <> (SELECT MAX(price) 
FROM articles);
```
1. Find the article with the largest price
2. Find the article with the second largest price
3. Find all the articles with the highest price
</details>

<details>
<summary>What's one downside of using a load balancer in a server setup?</summary>

1. It can become a performance bottleneck if it does not have enough resources.
2. It doesn't enable horizontal scaling of application servers.
3. It offers no protection against DDOS attacks since it doesn't limit client connections to a sensible amount and frequency.
</details>

<details>
<summary>What's true about adding servers to scale your backend?</summary>

1. It makes finding and fixing bugs more frustrating.
2. It makes adding and deploying new features easier.
3. It makes the server infrastructure easier to manage.
</details>

<details>
<summary>Which of the following patterns refers to creating duplicate objects while keeping performance in mind?</summary>

1. Decorator Pattern
2. Adapter Pattern
3. Prototype Pattern
4. Singleton Pattern
</details>

<details>
<summary>Which statement is true about the Decorator Pattern?</summary>

1. Refers to creating duplicate objects while keeping performance in mind.
2. Allows adding new functionality to an existing object without altering its structure.
3. Hides the complexities of the system and provides an interface to the client.
4. Is primarily used to reduce the number of objects created and to decrease memory footprint and increase performance.
</details>

<details>
<summary>Which statement is true about the Factory Pattern?</summary>

1. Refers to creating duplicate objects while keeping performance in mind.
2. Enables filtering a set of objects using different criteria and chaining them in a decoupled way through logical operations.
3. Is used where we need to treat a group of objects in a similar way as a single object.
4. Allows creating an object without exposing the creation logic to the client and refers to newly created object using a common interface.
</details>

<details>
<summary>Which statement is not true about promises?</summary>

1. A Promise has a .then() method.
2. A fulfilled or rejected promise will not change states.
3. A settled promise can become resolved.
4. A pending promise can become fulfilled, settled, or rejected.
</details>

<details>
<summary>What will be the output of the following Javascript code?</summary>

```javascript
const delay = ms => new Promise(res => setTimeout(res, ms));

async function asyncCallFirst() {
    await delay(3000);
    console.log('async call 1');
}

async function asyncCallSecond() {
	  await delay(1000);
  	console.log('async call 2');
}

(async() => {
  asyncCallFirst();
  await asyncCallSecond();
})();
```
1. "async call 1" "async call 2"
2. "async call 2" "async call 1"
3. An exception is raised.
4. Empty output.
</details>

<details>
<summary>What is the time, space complexity of the following code?</summary>

```javascript
int a = 0, b = 0;
for (i = 0; i < N; i++) {
    a = a + rand();
}
for (j = 0; j < M; j++) {
    b = b + rand();
}
```
1. O(N * M) time, O(1) space
2. O(N + M) time, O(N + M) space
3. O(N + M) time, O(1) space
4. O(N * M) time, O(N + M) space
</details>

<details>
<summary>The snippet is describing a common situation in computer science, what is it called?</summary>

```
Say we have 2 resources A and B used by processes X and Y :
- X starts to use A
- X and Y try to start using B
- Y 'wins' and gets B first
- now Y needs to use A
- A is blocked by X, which is waiting for Y
```
1. Race condition
2. Thread-safe
3. Deadlock
4. Starvation
</details>

<details>
<summary>Which of the following statements is true about Mutex?</summary>

1. A mutex ensures that the code being controlled will be hit by multiples threads at a time.
2. A mutex can be released only by the thread that had acquired it.
3. A mutex can be signaled by any thread (or process).
4. Starvation
</details>

<details>
<summary>How to prevent an SQL injection?</summary>

1. Prepared statements with parameterized queries
2. Use of stored procedures
3. Escaping All User Supplied Input
4. All of the above
</details>

<details>
<summary>When true about short polling (vs long polling, WebSockets)?</summary>

1. Short polling basically involves making an HTTP request to a server and then holding the connection open to allow the server to respond at a later time.
2. Using short polling means using less open connections.
3. Using short polling means making less requests to the server.
</details>

<details>
<summary>What's true about continuous integration?</summary>

1. Continuous integration means every change that passes all stages of your production pipeline is released to your customers
2. Continuous integration means deploying all code changes to a testing and/or production environment after the build stage.
3. Continuous integration means merging their changes back to the main branch as often as possible
</details>

<details>
<summary>What defintion best describes Spike Testing?</summary>

1. Spike testing is a type of stress testing when workloads are increased for short amounts of time.
2. Spike testing is a type of stress testing when workloads are increased for long and sustained amounts of time.
3. There is no such things as Spike Testing
</details>

<details>
<summary>What's the difference between faking, and stubbing?</summary>

1. Fake objects have working implementations, but usually take some shortcut which makes them not suitable for production.
2. Stubs provide canned answers to calls made during the test, usually not responding at all to anything outside what's programmed in for the test.
3. All of the above
</details>

<details>
<summary>What is the difference between JOIN and UNION?</summary>

1. JOIN allows us to “lookup” records on other table based on the given conditions between two tables. UNION operation allows us to add 2 similar data sets to create resulting data set that contains all the data from the source data sets.
2. UNION allows us to “lookup” records on other table based on the given conditions between two tables. JOIN operation allows us to add 2 similar data sets to create resulting data set that contains all the data from the source data sets.
3. None of the above
</details>

<details>
<summary>Complete the following SQL query for finding duplicate values in a SQL table?</summary>

```
SELECT
    name, email, COUNT(*)
 FROM
    users
GROUP BY
    name, email
HAVING
     /* YOUR ANSWER GOES HERE */
```
1. COUNT(*) < 1
2. COUNT(*) ≥ 1
3. COUNT(*) > 1
4. COUNT(*) = 0
</details>

<details>
<summary>What's true about NoSQL vs SQL databases?</summary>

1. SQL databases are easier to scale horizontally vs an equivalent NoSQL database.
2. NoSQL typically favors a normalized schema, whereas SQL favors a denormalized schema.
</details>

<details>
<summary>What's a common downside of database indexes?</summary>

1. They decrease performance on inserts and updates but not deletes
2. They decrease performance on deletes but not inserts and updates
3. They decrease performance on inserts, updates and deletes
</details>

<details>
<summary>Which statement is true about database mirroring and database replication?</summary>

1. Replication refers to keeping copies of database to a geographically different location.
2. Mirroring refers to creating multiple copies of data objects of a database for distribution efficiency.
3. The mirroring of a database costs higher than replication.
4. Mirroring can be easily implemented in case of distributed databases.
</details>
