# Inventory Management System Database Schema

## Overview

This GitHub repository contains the database schema for an Inventory Management System tailored to facilitate rental operations, item management, and user notifications. The schema is structured to support a variety of rental business models and is designed for high flexibility and efficiency.

## Schema Description

The database is comprised of interlinked tables designed to streamline the management of rental processes:

### Users
- **User Table**: Serves as a central repository for all user data, consolidating customer and staff information. It includes a `User_Type` attribute to differentiate between various user roles within the system.

### Rental Orders
- **Rental_Order Table**: Records the details of rental transactions, associating each order with a user and documenting the rental period and cost.

- **Rental_Order_Item Table**: Forms a many-to-many relationship between rental orders and items, accommodating multiple items per order and vice versa.

### Items
- **Item Table**: Lists all items in the inventory with detailed descriptions and cost information, linked to item types and statuses for improved categorization and status tracking.

- **Item_Type Table**: A categorization aid for items that simplifies item management and query optimization.

- **Status Table**: Maintains the current status of each item, vital for real-time inventory management and operational decisions.

### Notifications
- **Notification Table**: Manages the notification dispatch system, relating notifications to both users and specific rental orders, and categorizing them by type.

- **Notification_Type Table**: Defines the types of notifications that can be generated, offering a scalable solution for communication within the system.

## Design Decisions

The schema incorporates several design decisions that reflect best practices in database design:

- **Unified User Table**: By using a single table for all users, the schema allows for simplified user management and scalability.

- **Financial Data Integrity**: The `Total_Cost` fields use the `Decimal` data type to ensure precise financial representation.

- **Normalized Inventory Attributes**: Through lookup tables for item types and statuses, inventory data is kept normalized, reducing redundancy and simplifying updates.

- **Adaptable Notification Framework**: The notification system is designed to be adaptable, capable of handling a range of notification types and scenarios, and is linked to users and rental orders for relevant communication.

## ERD Overview

The Entity-Relationship Diagram (ERD) included in the repository visually details the structure and relationships of the database. It acts as a blueprint for the database's construction and guides ongoing development and maintenance.



![InventoryManagementERD](https://github.com/MikeProduce/InventoryMGMT-.NET-/assets/89554725/b5868d9a-cf21-4017-8c47-d90fe02e5170)

