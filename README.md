## **SQL Injection Payloads List**

### **SQL Injection**

In this section, we'll delve into the world of SQL injection, unveiling its intricacies and illustrating common attack vectors. We’ll explore techniques to identify and exploit diverse SQL injection vulnerabilities, while also providing essential strategies to safeguard against these critical threats.

### **What is SQL injection (SQLi)?**

SQL injection is a critical web security vulnerability that empowers attackers to manipulate the queries an application sends to its database. By exploiting this flaw, attackers can access sensitive data beyond their authorized reach, potentially exposing information belonging to other users or any data the application can access. This access can lead to unauthorized data modification or deletion, resulting in lasting alterations to the application's functionality and content.

Moreover, SQL injection attacks can escalate, enabling attackers to breach the underlying server or compromise other back-end infrastructure. In extreme cases, these attacks can even facilitate denial-of-service events, severely disrupting the availability of the application.

![Sql-Injection-Process](Image/sql-injection-process.svg)

| SQL Injection Type                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| In-band SQLi (Classic SQLi)              | In-band SQL Injection is the most common and straightforward type of attack. It occurs when the attacker uses the same communication channel to both inject malicious SQL queries and retrieve results. The two primary forms of in-band SQLi are Error-based SQLi and Union-based SQLi, both of which allow attackers to quickly gain insights or manipulate the database.                                                                                                                                                                                                                   |
| Error-based SQLi                         | This technique relies on error messages returned by the database server. The attacker can exploit these errors to gather information about the database structure, which might be enough to enumerate entire tables or databases without further exploitation.                                                                                                                                                                                                                                                                                                                                |
| Union-based SQLi                         | Union-based SQL Injection leverages the UNION SQL operator to combine the results of multiple SELECT statements into a single response. This technique enables attackers to retrieve multiple sets of data in one go by embedding malicious SQL queries into the original request.                                                                                                                                                                                                                                                                                                            |
| Inferential SQLi (Blind SQLi)            | Inferential SQL Injection is a more subtle attack method, where attackers dont directly retrieve data. Instead, they infer information based on the behavior of the database and application. Though it is slower than in-band SQLi, inferential SQLi is just as potent. It’s commonly called “blind SQL Injection” because the attacker receives no visible feedback. However, by sending specific queries and observing the applications response, the attacker can reconstruct the underlying database structure. There are two types: Boolean-based Blind SQLi and Time-based Blind SQLi. |
| Boolean-based (Content-based) Blind SQLi | In this technique, the attacker sends a query that forces the application to return different content based on whether the query returns a TRUE or FALSE value. By observing changes or no changes in the content of the HTTP response, attackers can determine the validity of their SQL query and infer information from the database.                                                                                                                                                                                                                                                      |
| Time-based Blind SQLi                    | Time-based Blind SQL Injection relies on the databases response time to indicate whether a query is valid. The attacker sends a query that forces the database to wait for a specified period before responding. If the response is delayed, the attacker knows the query returned TRUE; if it’s immediate, the result is FALSE. This technique allows attackers to extract data even when no information is returned by the application.                                                                                                                                                     |
| Out-of-band SQLi                         | Out-of-band SQL Injection is less common, as it relies on database features that aren’t always available. It occurs when the attacker uses a different channel for sending malicious queries and retrieving results, unlike in-band SQLi. This technique is particularly useful when in-band attacks are unreliable due to server instability or when features such as HTTP responses are delayed.                                                                                                                                                                                            |
| Voice-Based SQL Injection                | Voice-Based SQL Injection targets systems that interact with databases through voice commands. In this method, an attacker could exploit voice input systems by issuing malicious SQL queries through spoken commands, allowing unauthorized access to the database. As voice-controlled applications become more popular, this vector could potentially open new avenues for attackers.                                                                                                                                                                                                      |

## **Top SQL Injection Tools for Database Exploitation and Security Testing**

+ **[SQLMap](https://github.com/sqlmapproject/sqlmap)** – An advanced and highly automated SQL injection tool that allows full control over database takeovers. SQLMap is widely recognized for its powerful features, including the ability to detect and exploit                SQL injection vulnerabilities and provide an in-depth database fingerprinting, data retrieval, and even remote code execution.


+ **[jSQL Injection](https://github.com/ron190/jsql-injection)** – A lightweight and fast Java-based tool designed for automatic SQL injection. It simplifies the process of exploiting SQL injection vulnerabilities in databases, offering user-friendly features                        like database schema exploration, data extraction, and remote database modification.


+ **[BBQSQL](https://github.com/Neohapsis/bbqsql)** – A tool specifically designed for blind SQL injection exploitation. BBQSQL excels in situations where traditional SQL injection tools fail due to lack of visible output, providing robust methods to                    infer information from vulnerable databases without needing direct feedback.


+ **[NoSQLMa](https://github.com/codingo/NoSQLMap)** – A tool built for automating the detection and exploitation of NoSQL databases like MongoDB, CouchDB, and Redis. It brings the SQL injection concept to NoSQL databases, enabling the exploitation of                    improperly secured NoSQL instances through injection techniques.


+ **[Whitewidow](https://www.kitploit.com/2017/05/whitewidow-sql-vulnerability-scanner.html)** – A powerful SQL vulnerability scanner that quickly detects SQL injection vulnerabilities on websites. It automates the process of scanning large sets of URLs for SQLi weaknesses, making it an                          essential tool for pen testers and security professionals.


+ **[DSSS (Damn Small SQLi Scanner)](https://github.com/stamparm/DSSS)** – A compact yet efficient SQL injection scanner, ideal for quickly identifying SQL vulnerabilities in web applications. DSSS is designed for minimal resource usage, making it                                            perfect for lightweight tasks while maintaining strong detection capabilities.


+ **[Explo](https://github.com/dtag-dev-sec/explo)** – A versatile tool that reads and generates human and machine-readable web vulnerability testing reports. It helps security professionals and developers by automating SQL injection testing and generating               comprehensive vulnerability assessments.


+ **[Blind-SQL-Bitshifting](https://github.com/awnumar/blind-sql-bitshifting)** – A niche tool used for exploiting blind SQL injection vulnerabilities via bit-shifting techniques. This unique approach allows attackers to extract database information even in                                         restricted environments where traditional methods fail.


+ **[Leviathan](https://github.com/leviathan-framework/leviathan)** – A mass auditing toolkit designed to conduct wide-range security assessments. Leviathan offers capabilities for SQL injection testing, along with other mass auditing functions for web applications,                    making it a go-to for large-scale penetration tests.


+ **[Blisqy](https://github.com/JohnTroony/Blisqy)** – A specialized tool that exploits time-based blind SQL injection vulnerabilities found within HTTP headers, particularly targeting MySQL/MariaDB databases. Blisqy is efficient for detecting and                        exploiting time-delayed responses in SQL injections, making it suitable for harder-to-exploit scenarios.


These tools cover a broad spectrum of SQL injection and vulnerability testing scenarios, offering different methods and approaches to detect, exploit, and secure databases.


## **SQL Injection Payloads**








## **References and Additional Reading**

+ **Understanding SQL Injection (OWASP Guide):** A comprehensive introduction to SQL Injection vulnerabilities, including how they occur and ways to prevent them.
[Read More on OWASP SQL Injection](https://www.owasp.org/index.php/SQL_Injection)

+ **Exploring Blind SQL Injection:** This guide focuses on Blind SQL Injection, a more subtle but equally dangerous form of attack where the results are not directly visible.
[Learn About Blind SQL Injection](https://www.owasp.org/index.php/Blind_SQL_Injection)

+ **SQL Injection Testing Techniques (OTG-INPVAL-005):** A thorough overview of how to test for SQL injection vulnerabilities in web applications.
[SQL Injection Testing Guide](https://www.owasp.org/index.php/Testing_for_SQL_Injection_(OTG-INPVAL-005))

+ **Bypassing Web Application Firewalls (WAF) in SQL Injection Attacks:** Discover advanced techniques for bypassing security defenses such as WAFs in SQL injection exploits.
[Bypassing WAF in SQL Injection](https://www.owasp.org/index.php/SQL_Injection_Bypassing_WAF)

+ **Code Review for SQL Injection Vulnerabilities:** A detailed explanation of how to review source code to identify potential SQL injection vulnerabilities.
[Guide to Reviewing Code for SQL Injection](https://www.owasp.org/index.php/Reviewing_Code_for_SQL_Injection)

+ **PL/SQL Injection Explained:** Explore the specifics of SQL Injection in PL/SQL environments, a database procedural extension to SQL.
[PL/SQL SQL Injection Guide](https://www.owasp.org/index.php/PL/SQL:SQL_Injection)

+ **Testing for NoSQL Injection Vulnerabilities:** A guide for identifying and mitigating NoSQL injection, a variant of SQL injection that targets NoSQL databases.
[Testing for NoSQL Injection](https://www.owasp.org/index.php/Testing_for_NoSQL_injection)

+ **SQL Injection Prevention Cheat Sheet:** Best practices for defending against SQL injection, including parameterized queries, prepared statements, and more.
[Injection Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Injection_Prevention_Cheat_Sheet.html)

+ **SQL Query Parameterization Cheat Sheet:** A focused resource on using query parameterization to prevent SQL injection, one of the most effective security measures.
[Query Parameterization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Query_Parameterization_Cheat_Sheet.html)
