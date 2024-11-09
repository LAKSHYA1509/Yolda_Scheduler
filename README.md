
# Yolda-Scheduler

## About
Yolda-Scheduler is a full-stack web application designed to help you manage and schedule your events in one place. Built using **Spring Boot** for the back-end and **PostgreSQL** for the database, this application allows users to create, update, and view their schedules while receiving email notifications for event updates.

## Features
- **OAuth Authentication**: Users can securely log in and sign up via OAuth.
- **Event Management**: Create, update, and view your events with ease.
- **User-Friendly Interface**: A simple and responsive UI for easy event management.

## Tech Stack
- **Back-End**: Spring Boot
- **Database**: PostgreSQL
- **Front-End**: HTML, CSS, Thymeleaf
- **Authentication**: OAuth2 (Google, Facebook, etc.)
- **Email Notifications**: JavaMailSender for sending emails

## Getting Started

### Prerequisites
Before you begin, ensure you have the following installed:
- **Java 17 or higher**  
- **Maven** (for building the project)
- **PostgreSQL** (or your preferred relational database)

### Clone the Repository
```bash
git clone https://github.com/your-username/Yolda_Scheduler.git
```

### Set Up Database
1. Create a PostgreSQL database. For example, `scm20`.
2. Update the `application.properties` file with your database credentials:
    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/yolda_scheduler
    spring.datasource.username=your-username
    spring.datasource.password=your-password
    spring.jpa.hibernate.ddl-auto=update
    ```

### Run the Application
To run the application locally:
```bash
mvn spring-boot:run
```

The application will be available at `http://localhost:8080`.

## Endpoints

- **POST** `/user/login`: Login with OAuth.
- **GET** `/user/contacts/add`: Add a new event.
- **POST** `/user/contacts/add`: Save new event.
- **GET** `/user/contacts`: View all event.
- **POST** `/user/contacts/search`: Search contacts by name, email, or phone.
- **GET** `/user/contacts/update/{contactId}`: Update an existing event.
- **POST** `/user/contacts/update/{contactId}`: Save updated event.
- **DELETE** `/user/contacts/delete/{contactId}`: Delete a event.

## Contributing

Feel free to fork the repository, make changes, and submit a pull request. We welcome contributions!

## License
This project is licensed under the GNU 3.0 License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- **Spring Boot** for the back-end framework.
- **PostgreSQL** for the database.
- **Thymeleaf** for server-side rendering.



### Notes:
1. Replace `your-username` with your GitHub username.
2. Adjust the database configuration (`application.properties`) based on your local setup.
