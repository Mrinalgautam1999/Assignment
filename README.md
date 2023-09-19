# <h1 align = "center"> User Management </h1>

## Overview

This project, named "User Management System" is a robust Spring Boot application designed for managing user data efficiently. It provides a set of RESTful API endpoints that allow you to perform various operations on user records, such as adding, retrieving, updating, and deleting user information.

## Technologies Used

- **Framework:** Spring Boot
- **Language:** Java
- **Build Tool:** Maven

## Data Flow

### Controller

The Controller layer is responsible for handling incoming HTTP requests and delegating them to the appropriate services. It defines API endpoints for the following operations:

1. **Add Visitor:** `POST /Visitor`
2. **Get Count:** `GET /total/Count
3. **Get Count by visitorName:** `GET /api/v1/visitor-count-app/username/{userName}/count`

```java

@RestController
public class UPIHitController {
    @Autowired
    VisitorService visitorService;

    @PostMapping("Visitor")
    public String addVisitor(@RequestBody Visitor visitor){
        return visitorService.addVisitor(visitor);
    }

    @GetMapping("visitors")
    public List<Visitor> totalNumberOfVisitor(){
        return visitorService.visitorList();
    }

    @GetMapping("total/Count")
    public Integer getTotalCount(){
        return visitorService.getCount();
    }

    @GetMapping("api/v1/visitor-count-app/username/{userName}/count")
    public Integer totalEntrySingleUser(@PathVariable String userName){
        return visitorService.totalCount(userName);
    }
}

```

## Database Design

The project's database design includes tables for user management, with fields such as:

- `userId` (User ID)
- `userName` (User Name)


### ArrayList

The project utilizes the `ArrayList` data structure to store and manage lists of `User` objects in various parts of the application. `ArrayList` provides dynamic sizing and efficient element retrieval, making it suitable for storing user records and performing operations on them.

These data structures enable the application to organize and manipulate user data efficiently while maintaining data integrity.


## Project Summary

The User Management project is a robust Spring Boot application designed for efficient user data management. It offers a set of RESTful API endpoints for various user-related operations, including adding, retrieving, updating, and deleting user information.

### Key Technologies Used

- **Framework:** Spring Boot
- **Language:** Java
- **Build Tool:** Maven


    
