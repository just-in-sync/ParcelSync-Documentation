# Technical Documentation

**Version:** 1.000259 (MVP)
**Date:** March 30, 2026
**Maintainer:** Justin Anthony A. Aleta

**Target**: Future AppSheet developers or IT maintenance staff.

## A. System Architecture & Data Model

### Data Sources: List the Google Sheets and Google Forms used

- `Admins`: The manager of the condominium
- `Security Guards`: Reception who handles incoming deliveries
- `Buildings`: The building owned or handled by the admin
- `Tenants`: Occupants of the units inside the condominium
- `Authorized Persons`: Helper to claim the packages of official tenants
- `Delivery logs`: The list of deliveries that goes to the condominium
- `Incoming Authorized Persons`: Table served as fetching necessary information of authorized persons
- `Archive Delivery Logs`: The archive sheet of the delivery logs

### Table Relationships

- The `Tenants`, `Admins`, and `Security Guards` have relationship to `Buildings` table.
- The `Tenants` and `Security Guards` table have relationship with `Delivery logs`
- The `Tenants` and the `Authorized Persons` have direct relationship with each other.

## B. Automations

1. Generate QR Delivery logs bot
2. Claimed Package Notification
3. Sending Reminder Notification
4. Authorized Person Invite bot
5. Weekly Report Notification
6. Archiving Notification

## C. Reference Views

1. Claim Form
2. Delivery Statistics

### Slices

1. **Arrived Deliveries to Claim**: This is filtered `Delivery logs` for packages with the `status` of "_Unclaimed_".
2. **Not yet approved**: This is filtered `Incoming Authorized Person` for packages with the `isApproved` of "_Unclaimed_".
