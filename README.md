# 🌩️ Nimbus Submission — Web Applications Using Servlets and JSP

This project contains **three independent web applications** demonstrating Servlets, JSP, and JDBC for handling user inputs, connecting to databases, and generating dynamic web content.
Each part can be deployed separately on **Apache Tomcat** or run together in a single server environment.

---

## 🧩 Part A — User Login (Servlet + HTML)

**Objective:** Build a simple login form validated by a Java Servlet.

**Features:**

* HTML login page
* Servlet validates hardcoded credentials
* Displays a personalized success message

**How to Run:**

1. Copy `PartA_UserLogin` into Tomcat’s `webapps` folder.
2. Start Tomcat.
3. Open: `http://localhost:8080/PartA_UserLogin/login.html`
4. Login:

   * **Username:** admin
   * **Password:** 12345

---

## 🧩 Part B — Employee Records Viewer (Servlet + JDBC)

**Objective:** Fetch and display employee details from a MySQL database.

**Employee Table:**

```sql
CREATE TABLE Employee (
  EmpID INT PRIMARY KEY,
  Name VARCHAR(50),
  Salary DECIMAL(10,2)
);
```

**Features:**

* View all employee records
* Search employee by ID
* Display results in an HTML table

**How to Run:**

1. Run the SQL script to create the Employee table in MySQL.
2. Update DB credentials in `EmployeeServlet.java`.
3. Copy `PartB_EmployeeRecords` to `webapps`.
4. Open: `http://localhost:8080/PartB_EmployeeRecords/employees.html`

---

## 🧩 Part C — Student Attendance Portal (JSP + Servlet + JDBC)

**Objective:** Build an attendance submission portal using JSP for input and Servlets for processing.

**Attendance Table:**

```sql
CREATE TABLE Attendance (
  StudentID INT,
  AttendanceDate DATE,
  Status VARCHAR(10)
);
```

**Features:**

* JSP form to enter attendance
* Servlet inserts records into MySQL
* JSP displays success message

**How to Run:**

1. Create the Attendance table in MySQL.
2. Update DB credentials in `AttendanceServlet.java`.
3. Copy `PartC_AttendancePortal` to `webapps`.
4. Open: `http://localhost:8080/PartC_AttendancePortal/attendance.jsp`

---

## 🧠 Concepts Demonstrated

| Part | Concept                          | Tech Used           |
| ---- | -------------------------------- | ------------------- |
| A    | Handling form data with Servlets | HTML, Servlet       |
| B    | Database access via JDBC         | Servlet, MySQL      |
| C    | MVC with JSP + Servlet           | JSP, Servlet, MySQL |

---

## 🚀 Running All Parts Together

1. Ensure MySQL is running and both tables are created.
2. Place all three folders inside Tomcat’s `webapps` directory.
3. Start Tomcat (`startup.bat` / `startup.sh`).
4. Access the applications:

   * Login: `http://localhost:8080/PartA_UserLogin/login.html`
   * Employees: `http://localhost:8080/PartB_EmployeeRecords/employees.html`
   * Attendance: `http://localhost:8080/PartC_AttendancePortal/attendance.jsp`
