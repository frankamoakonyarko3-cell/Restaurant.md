# Restaurant Management System

## Context Diagram

```mermaid
flowchart LR

    Customer[Customer]
    Staff[Restaurant Staff]
    Admin[Administrator]
    Payment[Payment Gateway]
    Email[Email/SMS Service]

    System((Restaurant Management System))

    Customer -->|Login / Register| System
    Customer -->|View Menu| System
    Customer -->|Place Order| System
    Customer -->|Make Payment| System
    Customer -->|Track Order| System

    System -->|Menu Information| Customer
    System -->|Order Confirmation| Customer
    System -->|Order Status| Customer

    Staff -->|View Orders| System
    Staff -->|Update Order Status| System
    System -->|Customer Orders| Staff

    Admin -->|Manage Menu| System
    Admin -->|Manage Users| System
    Admin -->|View Reports| System
    System -->|Reports| Admin

    System -->|Payment Request| Payment
    Payment -->|Payment Result| System

    System -->|Send Confirmation| Email
