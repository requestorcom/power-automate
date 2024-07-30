# Requestor

[Requestor](https://www.requestor.com) is a versatile multichannel helpdesk designed for customer support and internal request management. With Requestor, you can efficiently handle customer support and internal team requests through email, phone, and chat, all in one convenient location.

This connector is built on top of Requestor APIs and Webhooks and is intended for Requestor operators to manage tickets and contacts via Microsoft Power Automate.

## Publisher

requestor.com s.r.o.

## Prerequisites

You will need the following to proceed:

* To be a Requestor customer (Cloud or On-prem) with Requestor REST API available from the internet
* A user account in the Requestor application that has the required permissions to perform the operations that are defined in the flow(s), e.g. user access, ticket access, etc.

## Authentication

The connector uses basic authentication (username and password) to access the REST API of the Requestor application.

## Supported Operations

The Requestor connector supports the following operations:

### Triggers

All triggers are designed so that when the flow is saved, it creates an automation webhook in the Requestor application that is triggered when the particular operation happens.

- **When a ticket is created** (`TicketCreated`)
  - Triggers when a new ticket is created in the Requestor application.

- **When a user is created** (`UserCreated`)
  - Triggers when a new user is created in the Requestor application.

- **Ticket Monitoring** (`TicketMonitoring`)
  - Creates a generic automation webhook for ticket monitoring. Note: This webhook must be modified in the Requestor application to actually monitor specific events.

- **When a ticket state changes** (`TicketStateChange`)
  - Triggers when the state of a ticket changes in the Requestor application.

- **When a ticket category is changed** (`TicketCategoryChange`)
  - Triggers when the category of a ticket changes in the Requestor application.

- **Ticket Custom Form Change** (`TicketCustomFormChange`)
  - Triggers when a custom form associated with a ticket changes in the Requestor application.

- **When a user is updated** (`UserUpdated`)
  - Triggers when a user is updated in the Requestor application.

- **When a user is deleted** (`UserDeleted`)
  - Triggers when a user is deleted in the Requestor application.

- **When a company is created** (`CompanyCreated`)
  - Triggers when a new company is created in the Requestor application.

- **When a company is updated** (`CompanyUpdated`)
  - Triggers when a company is updated in the Requestor application.

- **When a company is deleted** (`CompanyDeleted`)
  - Triggers when a company is deleted in the Requestor application.

### Actions

- **Create Ticket** (`CreateTicket`)
  - Creates a new ticket in the Requestor application.

- **Create User** (`CreateUser`)
  - Creates a new user in the Requestor application.

### Internal Actions

These actions are used to support the configuration and cannot be directly used in the flow.

- **Get Services** (`GetServices`)
  - Retrieves a list of available services in the Requestor application.

- **Get Ticket Types** (`GetTicketTypes`)
  - Retrieves a list of available ticket types in the Requestor application.

- **Delete Trigger** (`DeleteTrigger`)
  - Deletes a specified trigger in the Requestor application.
