# Kaiburr Assessment 2025 - Task 1 Submission

**Candidate Name:** Dharanya D

---

## Objective

Java Spring Boot REST API for managing "task" objects stored in MongoDB.  
Includes endpoints for creating, listing, searching, deleting, and running tasks as required in the Kaiburr assessment.

---

## How to Compile and Run

1. **Start MongoDB database:**
    - Open Command Prompt and run:
      ```
      mongod
      ```
    - Wait for the message: `Waiting for connections`.

2. **Clone this repository and open it in IntelliJ IDEA.**

3. **Build the project:**
    - Use IntelliJ's build command or run:
      ```
      mvn clean install
      ```

4. **Run the backend server:**
    - Launch `TaskapiApplication.java`.
    - Wait for log output: `Started TaskapiApplication` and `Tomcat started on port 8080`.

5. **Test the API using Postman or your browser.**
    - Base URL: `http://localhost:8080`

---

## API Endpoints

| Method | URL                                    | Description                                         |
|--------|----------------------------------------|-----------------------------------------------------|
| GET    | /tasks                                 | List all tasks                                      |
| POST   | /tasks                                 | Create a new task                                   |
| GET    | /tasks/{id}                            | Get a task by ID (returns 404 if not found)         |
| DELETE | /tasks/{id}                            | Delete a task by ID                                 |
| GET    | /tasks/search?name=Assessment Task     | Search tasks by name (case-insensitive, contains)   |

**Sample POST Body:**

<pre>{ 
"name": "Assessment Task",
"owner": "Dharanya D",
"command": "echo Hello Kaiburr",
"taskExecutions": [] 
}  </pre>
## Embedded Screenshots

1. **MongoDB running (Command Prompt):**
   ![mongodb](output/mongodb.png)

2. **Spring Boot started (IntelliJ console):**
   ![springboot](output/springboot.png)

3. **POST /tasks (add new task):**
   ![posttasks](output/posttask.png)

4. **GET /tasks (task list):**
   ![gettasks](output/gettask.png)

5. **DELETE /tasks/{id}:**
   ![delete](output/delete.png)
