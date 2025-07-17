# Lab 6: Define Your REST API Endpoints
**Zoo Simulator API Design**  
**By Dzelle Faith Tan**

In this lab, I designed and documented the REST API endpoints for the Zoo Simulator.

This API definition ensures clarity, consistency, and maintainability for the system’s development, especially in the controller and service layers.

Each endpoint is structured with:
- **Resource** — The entity managed by the API
- **HTTP Verb** — The HTTP method used for the action
- **Resource URL** — The RESTful URL path with `{id}` placeholders
- **Use Case** — The purpose of the endpoint

---

## API Endpoints

| Resource | HTTP Verb | Resource URL | Use Case |
|---|---|---|---|
| **Tickets** | POST | `zoos/{id}/visitors/{id}/tickets` | Visitor buys a ticket |
|  | GET | `zoos/{id}/tickets/{id}` | Show a valid ticket |
| **Visitors** | POST | `zoos/{id}/visitors` | Add a new visitor |
|  | GET | `zoos/{id}/visitors/{id}/tasks` | Visitors can select from tasks |
| **Enclosures** | GET | `zoos/{id}/enclosures/{id}` | Visit an enclosure |
| **Animals** | POST | `zoos/{id}/enclosures/{id}/animals/{id}/feeds` | Feed an animal |
| **Shops** | GET | `zoos/{id}/buildings/{id}/shops/{id}` | Visit a shop |
|  | POST | `zoos/{id}/buildings/{id}/shops/{id}/items/{id}/purchases` | Make a purchase |
| **Hospitals** | POST | `zoos/{id}/buildings/{id}/hospitals/{id}/lectures/{id}/visits` | Visit the hospital lecture |
| **Visitors** | DELETE | `zoos/{id}/visitors/{id}` | Leave the zoo |

---

## Other API Endpoints

| Resource | HTTP Verb | Resource URL | Use Case |
|---|---|---|---|
| **Visitors** | GET | `zoos/{id}/visitors` | Get all visitors |
|  | POST | `zoos/{id}/visitors` | Add a new visitor |
|  | PUT | `zoos/{id}/visitors/{id}` | Update visitor personal data |
|  | DELETE | `zoos/{id}/visitors/{id}` | Visitor leaves the zoo |
|  | PATCH | `zoos/{id}/visitors/{id}` | Update visitor status |
|  | HEAD | `zoos/{id}/visitors/{id}` | Check if visitor exists |
| **Tickets** | GET | `zoos/{id}/tickets` | Get all tickets |
|  | POST | `zoos/{id}/visitors/{id}/tickets` | Visitor buys a ticket |
|  | PUT | `zoos/{id}/visitors/{id}/tickets/{id}` | Modify ticket information |
|  | DELETE | `zoos/{id}/visitors/{id}/tickets/{id}` | Delete a visitor's ticket |
|  | PATCH | `zoos/{id}/visitors/{id}/tickets/{id}` | Update ticket (e.g., timestamp) |
|  | HEAD | `zoos/{id}/visitors/{id}/tickets/{id}` | Check if ticket exists |
| **Buildings** | GET | `zoos/{id}/buildings` | Get all buildings |
|  | POST | `zoos/{id}/buildings` | Add a building |
| **Shops** | GET | `zoos/{id}/shops` | Get all shops |
|  | POST | `zoos/{id}/buildings/{id}/shops/{id}/visits` | Visitor visits a shop |
|  | POST | `zoos/{id}/buildings/{id}/shops/{id}/purchases` | Visitor makes a purchase |
| **Hospitals** | POST | `zoos/{id}/buildings/{id}/hospitals/{id}/lecture/{id}/visits` | Attend a hospital lecture |
| **Enclosures** | GET | `zoos/{id}/enclosures` | Get all enclosures |
|  | GET | `zoos/{id}/enclosures/{id}` | Visit/view a specific enclosure |
| **Animals** | POST | `zoos/{id}/enclosures/{id}/animals/{id}/feeds` | Handler feeds an animal |
|  | POST | `zoos/{id}/enclosures/{id}/animals/{id}/exercises` | Handler exercises an animal |
|  | POST | `zoos/{id}/enclosures/{id}/animals/{id}/examines` | Handler examines an animal |
|  | POST | `zoos/{id}/hospitals/{id}/animals/{id}/heals` | Veterinarian heals an animal |
|  | POST | `zoos/{id}/hospitals/{id}/lectures` | Veterinarian lectures |
| **Zoo** | POST | `zoos/{id}/opens` | Manager opens the zoo |
|  | POST | `zoos/{id}/closes` | Manager closes the zoo |

