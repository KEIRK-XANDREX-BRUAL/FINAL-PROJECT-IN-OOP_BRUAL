# Immunization Tracker System 🏥
   *Vaccine Management System*

## I. Project Overview

The Vaccine Management System (VMS) is a Java-based console application designed to streamline the management of vaccination records for healthcare providers. It helps efficiently organize patient information and ensures accurate tracking of vaccination schedules for different patient categories: children, teens, and adults. It ensures efficient record-keeping and provides critical features like tracking vaccination schedules, administering vaccines, and monitoring vaccination completion statuses.

The project demonstrates the core principles of Object-Oriented Programming (OOP), including **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**, in a practical, real-world context. By addressing healthcare needs, the project aligns with SDG 3: Good Health and Well-being, emphasizing the importance of timely and complete vaccinations for better health outcomes.

---

### Objectives 🎯

The **Immunization Tracker System** aims to:

1. **Manage Patient Records**: Organize patient information by category (Children, Teens, Adults) and enable easy access and editing.
2. **Track Vaccination Schedules**: Monitor vaccine administration and calculate the next vaccination date automatically.
3. **Maintain Vaccination History**: Provide detailed records of each patient's vaccination status and history.
4. **Enhance Healthcare Efficiency**: Automate record-keeping to reduce manual workload and minimize errors.
5. **Support SDG 3**: Ensure timely vaccinations to improve public health and reduce preventable diseases.

## Key Features 🚀

#### 1. **Patient Management**  ⚕️
   - Effortlessly manage patient records by adding, viewing, and editing information.
   - Categorize patients into **Children**, **Teens**, and **Adults**, with unique fields for each:
     - **Children**: Includes parent or guardian information.
     - **Teens**: Tracks the school name.
     - **Adults**: Records the patient’s occupation.

#### 2. **Vaccination Tracking** 🩺
   - Administer vaccines with real-time tracking:
     - Monitor the number of doses administered.
     - Track the remaining doses for each vaccine.
   - Automatically calculate and update the **next vaccination date** based on the selected vaccine's schedule (e.g., 6 months or 1 year later).
   - Ensure patients are fully vaccinated with completion status indicators.

#### 3. **Vaccination Records**
   - View comprehensive vaccination histories for each patient:
     - Includes vaccine names, doses administered, completion statuses, and the next scheduled dose.
   - Organize records by patient type for easy navigation.

#### 4. **Dynamic and User-Friendly Menus**
   - Intuitive console-based menus:
     - Tailored options for different operations (e.g., patient management, vaccine administration).
     - Clear prompts and structured design for a seamless user experience.
   - Robust error handling to ensure smooth operation and informative feedback for invalid inputs.

#### 5. **Efficient and Scalable Design**
   - Built using Object-Oriented Programming principles to ensure:
     - Code reusability and scalability for future enhancements.
     - Organized and modular functionality for easy maintenance.
   - Abstracted vaccine and patient data management for clear separation of concerns.

## II. How OOP Principles Were Applied 📋

### 1. **Encapsulation**
   - **Implementation**: Patient and vaccine data are stored as private fields, accessible only through public getter and setter methods. This ensures data integrity and protects sensitive information.
   - **Example**: 
     ```java
     protected String firstName;
     public String getFirstName() {
         return firstName;
     }
     public void setFirstName(String firstName) {
         this.firstName = firstName;
     }
     ```

### 2. **Inheritance**
   - **Implementation**: A `PatientDetails` base class defines common properties (e.g., ID, name, age, contact). Specific patient types (`ChildPatient`, `TeenPatient`, `AdultPatient`) extend this base class and add unique attributes like parent name, school name, or occupation.
   - **Example**: 
     ```java
     public class TeenPatient extends PatientDetails {
         private String schoolName;
         // Additional functionality specific to teens
     }
     ```

### 3. **Polymorphism**
   - **Implementation**: The system uses method overriding to customize behavior based on patient types. For instance, `displayPatientInfo()` provides tailored output for each category.
   - **Example**:
     ```java
     public void displayPatientInfo() {
         System.out.println("Name: " + firstName + " " + lastName);
         System.out.println("Parent Name: " + ((ChildPatient) this).getParentName());
     }
     ```

### 4. **Abstraction**
   - **Implementation**: Abstract classes and interfaces are used to hide implementation details while exposing essential functionalities. For example, the `PatientDetails` class abstracts common behaviors across patient types.
   - **Example**:
     ```java
     public abstract class PatientDetails {
         public abstract void displayPatientInfo();
     }
     ```

---

## III. SDG Integration 🌍

The project aligns with **Sustainable Development Goal 3 (Good Health and Well-being)** by supporting timely and complete vaccinations. By tracking doses and schedules, the system ensures that patients stay up to date with their vaccinations, reducing the risk of preventable diseases. This directly contributes to healthier communities and improved global health outcomes.

---

## IV. Instructions for Running the Program ⚙️

### 1. Prerequisites
   - Install **Java Development Kit (JDK 8 or later)** from the [official Java website](https://www.oracle.com/java/technologies/javase-downloads.html).
   - Install **Visual Studio Code** or any Java-compatible IDE for running and debugging the project.

### 2. Download and Extract the Project
   - Download the ZIP file containing the project from the repository.
   - Extract the ZIP file to a folder on your computer.

### 3. Open the Project
   - Open the extracted folder in Visual Studio Code or your chosen IDE.

### 4. Compile the Code
   - Open the terminal in the project directory and compile all Java files using:
     ```bash
     javac Main.java
     ```

### 5. Run the Program
   - Execute the program using:
     ```bash
     java Main
     ```

   - Follow the on-screen instructions to manage patient and vaccination records.

---

