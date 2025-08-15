# Personal Finance Management Backend

A backend application for managing personal finances, built with Spring Boot and containerised using Docker. The system
implements the CQRS (Command Query Responsibility Segregation) pattern to separate write and read operations, ensuring
scalability and maintainability.

## Project Overview

**This backend system allows users to:**

* Record income and expenses.
* Define budgets and financial goals.
* Retrieve financial reports and spending analytics.

**The application adopts the CQRS pattern:**

* Command Module: Handles all write operations like adding, updating, and deleting data.
* Query Module: Handles all read operations like fetching transaction history, budget utilisation, and reports.

## Features

**Command Module:**

* Add, edit, and delete transactions.
* Create and manage budgets.
* Define financial goals.

**Query Module:**

* Fetch transaction history.
* Retrieve real-time budget utilisation.
* Generate detailed financial reports.

## Technologies Used

## Architecture

The project follows a modular design with clear separation of concerns:

**1. Command Module:**

* Handles all data-modifying operations.
* Publishes events to RabbitMQ for synchronising the query-side database.

**2. Query Module:**

* Handles data retrieval and analytics.
* Subscribes to events from RabbitMQ to update the read-side database.

Note: R&D all best practice for both database synchronization

**3. Databases:**

* PostgreSQL: Write-side database for transactional consistency.
* MongoDB: Read-side database for fast data retrieval.

**4. Message Broker:**

* RabbitMQ is used for communication between the command and query modules.

Note: R&D all best practice for both database synchronization

<details>
  <summary>Click to expand/collapse</summary>
  This is the content that will be hidden by default and revealed when the summary is clicked.
  You can include multiple lines, code blocks, or other Markdown elements here.
</details>