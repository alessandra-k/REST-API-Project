# REST API (Group Academic Project)

The REST API project is a secure, role-based application that manages various administrative and student-related data. It offers RESTful endpoints that allow both administrative users and regular students to interact with the system based on their roles.

---

### **Key Features**
- **Entities and Their Relationships:**
  - **Students:** Represents students, linking them to memberships and peer tutor roles.
  - **Courses:** Manages academic courses, capturing course details and associated peer tutors.
  - **Clubs:** Differentiates between academic and non-academic clubs using discriminator values.
  - **Memberships:** Links students to clubs through a relationship entity, `ClubMembership`.
  - **Peer Tutors:** Represents student tutors and their course registrations (`PeerTutorRegistration`).

- **Security Implementation:**
  - Secured API endpoints using `@RolesAllowed` annotations.
  - Designed `SecurityUser` and `SecurityRole` entities to manage user roles and permissions.
  - Implemented a custom authentication mechanism with hashed passwords (PBKDF2 algorithm).
  - Enforced role-based access control:
    - **ADMIN_ROLE:** Full access to all API features.
    - **USER_ROLE:** Restricted access to personal and limited shared data.

- **Additional Features:**
  - **Lazy Loading:** Prevented unnecessary data loading; used `JOIN FETCH` for associated entities in specific queries.

---

## **Code Contributions**

The project was developed as a group assignment. The college provided the initial codebase, including partially implemented entities and configurations. Our contributions include:

1. Completing TODOs to:
   - Integrate the custom authentication mechanism with the database.
   - Map relationships between entities, such as the one-to-one relationship between `SecurityUser` and `Student`.
   - Implement business logic for role-based access control.
2. Enhancing CRUD functionalities with proper data validation and error handling.
3. Testing the API with Postman and creating JUnit test cases for validation.
4. Writing Named Queries for specific data retrieval needs.
5. Securing RESTful endpoints with Java EE Security.

---

## **REST API Endpoints**

### **Entities**
- `Students`: Manage student data (create, retrieve, update, delete).
- `Courses`: Handle course details and peer tutor assignments.
- `Clubs`: Manage academic and non-academic student clubs.
- `Memberships`: Link students to clubs with `ClubMembership`.

---

## **Technologies Used**

- **Java EE**: Core framework for building enterprise applications.
- **Programming Language**: Java
- **Specifications**: JAX-RS (RESTful services), EJB (business logic), JPA (ORM and persistence)
- **Security**: Java EE Security (role-based authentication)
- **Database**: MySQL
- **Application Server**: Payara
- **Testing Tools**: Postman

---

## **Acknowledgments**

This project was part of the **Enterprise Application Programming** course at Algonquin College. While the base code was provided, we implemented features and completed the remaining functionalities.

- **Contributors:**
  - Alessandra Prunzel Kittlaus
  - Alex Hulford
  - Andres Camilo Porras Becerra
  - Sewuese Ayu
