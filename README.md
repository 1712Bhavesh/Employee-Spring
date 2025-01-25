### **Project README: Full-Stack Employee Management System**  

---

#### **Project Overview**  
This project is a full-stack Employee Management System implementing CRUD functionality using **Spring Boot** for the backend and **Angular 18** with Angular Material for the frontend. It connects to a **MySQL database** for storing employee-related data and uses **REST APIs** for communication between the frontend and backend. The application also supports advanced features like filtering, sorting, and pagination.

---

#### **Key Features**  
- **Backend:** Spring Boot application with REST API to handle CRUD operations (Create, Read, Update, Delete).  
- **Frontend:** Angular 18 standalone application using Angular Material for UI components.  
- **Database:** MySQL database to store and manage employee data.  
- **Testing:** Postman for testing REST API endpoints.  
- **Advanced Features:** Material table with searching, sorting, and pagination.  

---

#### **Tech Stack and Libraries**  
1. **Backend:**
   - **Spring Boot:** Framework for developing the backend application.  
   - **Spring Web:** To create REST APIs.  
   - **Spring Data JPA:** For database operations.  
   - **MySQL Driver:** JDBC driver for connecting to the MySQL database.  
   - **Lombok:** For reducing boilerplate code (e.g., Getters and Setters).  
   - **Maven:** Dependency management and build tool.  

2. **Frontend:**
   - **Angular 18:** Framework for building the frontend application.  
   - **Angular Material:** Library for UI components (Material Table, Dialog, Buttons, etc.).  
   - **HttpClient Module:** For HTTP communication with the backend APIs.  

3. **Database:**  
   - **MySQL Database:** Managed through XAMPP Control Panel.  

4. **Testing Tools:**  
   - **Postman:** For testing REST API endpoints.  

---

#### **Setup Instructions**  
1. **Database Setup:**  
   - Install XAMPP and launch the MySQL service.  
   - Use the XAMPP control panel to create a database (e.g., `employee_db`).  
   - Create a table named `employee` with the required fields.

2. **Backend Setup:**  
   - Clone the Spring Boot backend repository.  
   - Update the `application.properties` file with your MySQL credentials:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
     spring.datasource.username=root
     spring.datasource.password=your_password
     spring.jpa.hibernate.ddl-auto=update
     ```
   - Build and run the application using Maven or your IDE.  

3. **Frontend Setup:**  
   - Install Node.js and Angular CLI if not already installed.  
   - Clone the Angular frontend repository.  
   - Navigate to the project directory and install dependencies:
     ```bash
     npm install
     ```
   - Set up a proxy configuration in `proxy.conf.json` to enable communication with the backend:
     ```json
     {
       "/api": {
         "target": "http://localhost:8080",
         "secure": false
       }
     }
     ```
   - Start the development server:
     ```bash
     ng serve --open
     ```

---

#### **Implementation Details**  
1. **Backend (Spring Boot):**  
   - Create REST endpoints for `GET`, `POST`, `PUT`, and `DELETE` requests.  
   - Use Spring Data JPA for database interaction.  

2. **Frontend (Angular):**  
   - Install Angular Material for UI components:
     ```bash
     ng add @angular/material
     ```
   - Generate required components, services, and modules:
     ```bash
     ng generate component home
     ng generate service employee
     ```
   - Implement CRUD operations using Angular's **HttpClient** module.  

3. **UI Features:**  
   - Create an Angular Material table and populate it with API data.  
   - Add action buttons (`Edit` and `Delete`) to each row in the table.  
   - Use **Material Dialog** to implement Create and Edit functionality.  
   - Add sorting, filtering, and pagination using Angular Material options.  

4. **Testing:**  
   - Test the REST APIs using Postman to ensure correct functionality.  
   - Verify frontend features, such as data display, form submissions, and table interactions.  

#### **How to Use the Application**  
1. Navigate to the homepage of the Angular app.  
2. View the employee list in the material table.  
3. Use the **Create** button to add a new employee via the Material Dialog form.  
4. Edit or delete existing employees directly from the table.  
5. Use search, sorting, and pagination to explore the employee data.  
