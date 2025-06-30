#  System Operation Analysis

A complete analysis of CRUD operations across six different systems, focusing on how actions are handled in the **Frontend**, **Backend**, and **Database** layers. This document is useful for understanding system architecture, business logic flow, and the division of responsibilities in software systems.

---

## 📚 Table of Contents

- [ Bank System](#-bank-system)
- [ Hospital System](#-hospital-system)
- [ Hotel System](#-hotel-system)
- [ Airline System](#️-airline-system)
- [ E-Commerce System](#-e-commerce-system)
- [ YouTube-like System](#-youtube-like-system)

---

## 🏦 Bank System

| Operation | Example              | Role                      | Frontend         | Backend                    | Database               |
|----------:|----------------------|---------------------------|------------------|----------------------------|------------------------|
| Insert    | Open new account     | Extra (Manager approval)  | Form submission  | Validation, create ID      | Insert into `Accounts` |
| Delete    | Close account        | Extra (Pending dues check)| Request delete   | Check dues                 | Remove from `Accounts` |
| Update    | Change contact info  | Direct                    | Edit profile     | Validate, log changes      | Update `Customers`     |
| Query     | View balance         | Direct                    | Dashboard        | Call API                   | Fetch from `Accounts`  |

---

## 🏥 Hospital System

| Operation | Example                | Role                   | Frontend         | Backend               | Database               |
|----------:|------------------------|------------------------|------------------|-----------------------|------------------------|
| Insert    | Add new patient        | Direct                 | Registration form| ID generation         | Insert into `Patients` |
| Delete    | Remove discharged record| Extra (Doctor approval)| Button           | Check summary         | Delete from `Admissions`|
| Update    | Change treatment plan  | Extra (Doctor role)    | Doctor panel     | Log change            | Update `Treatment`     |
| Query     | View patient history   | Direct                 | Search field     | Fetch records         | Join `Visits`, `Medications` |

---

## 🏨 Hotel System

| Operation | Example               | Role    | Frontend        | Backend                | Database               |
|----------:|-----------------------|---------|------------------|------------------------|------------------------|
| Insert    | Book a room           | Direct | Booking form     | Room check, reserve    | Insert into `Reservations` |
| Delete    | Cancel booking        | Direct | Cancel button    | Check policy           | Delete from `Reservations` |
| Update    | Modify reservation    | Direct | Edit option      | Recheck availability   | Update `Reservations` |
| Query     | View available rooms  | Direct | Date picker      | Filter logic           | Fetch from `Rooms`     |

---

## ✈️ Airline System

| Operation | Example                | Role                   | Frontend            | Backend             | Database            |
|----------:|------------------------|------------------------|---------------------|---------------------|---------------------|
| Insert    | Book a flight          | Direct                 | Booking UI          | Seat allocation     | Insert into `Bookings` |
| Delete    | Cancel flight          | Extra (Refund policy)  | Cancel request      | Validate timing     | Delete from `Bookings` |
| Update    | Change passenger info  | Direct                 | Profile update      | Validate            | Update `Passengers` |
| Query     | View flight schedule   | Direct                 | Filter UI           | Process request     | Select from `Flights` |

---

## 🛒 E-Commerce System

| Operation | Example                  | Role                   | Frontend        | Backend                    | Database              |
|----------:|--------------------------|------------------------|------------------|----------------------------|-----------------------|
| Insert    | Add to cart              | Direct                 | Product page     | Store session/cart ID      | Insert into `CartItems` |
| Delete    | Cancel order             | Extra (Warehouse check)| Cancel button    | Check status               | Remove from `Orders` |
| Update    | Change shipping address  | Direct                 | Address form     | Validate                   | Update `Customers`    |
| Query     | Search product           | Direct                 | Search bar       | Query parser               | Select from `Products` |

---

## 📺 YouTube-like System

| Operation | Example              | Role     | Frontend     | Backend                | Database               |
|----------:|----------------------|----------|--------------|------------------------|------------------------|
| Insert    | Upload new video     | Direct   | Upload UI    | File compression, save | Insert into `Videos`   |
| Delete    | Remove video         | Direct   | Delete button| Remove file, log       | Delete from `Videos`   |
| Update    | Change video title   | Direct   | Edit info    | Validation             | Update `Videos`        |
| Query     | Search videos        | Direct   | Search bar   | Keyword match          | Select from `Videos`, `Tags` |


