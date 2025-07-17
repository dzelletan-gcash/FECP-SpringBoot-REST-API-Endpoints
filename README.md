# Lab 6: Define Your REST API Endpoints
**Zoo Simulator API Design**  
**By Dzelle Faith Tan**

In this lab, I designed and documented the REST API endpoints for the Zoo Simulator.  

This API definition ensures clarity, consistency, and maintainability for the system’s development, especially in the controller and service layers.

Each endpoint is structured with:
- **Resource** — The entity managed by the API
- **HTTP Verb** — The HTTP method used for the action
- **Resource URL** — The RESTful URL path
- **Use Case** — The purpose of the endpoint

---

## API Endpoints

| Resource | HTTP Verb | Resource URL | Use Case |
|---|---|---|---|
| **Tickets** | POST | `zoos/1/visitors/4/tickets` | Visitor buys a ticket |
|  | GET | `zoos/1/tickets/2` | Show a valid ticket |
| **Visitors** | POST | `zoos/1/visitors` | Add a new visitor |
|  | GET | `zoos/1/visitors/2/tasks` | Visitors can select from tasks |
| **Enclosures** | GET | `zoos/1/enclosures/4` | Visit an enclosure |
| **Animals** | POST | `zoos/1/enclosures/4/animals/2/feeds` | Feed an animal |
| **Shops** | GET | `zoos/1/buildings/1/shops/2` | Visit a shop |
|  | POST | `zoos/1/buildings/1/shops/2/items/2/purchases` | Make a purchase |
| **Hospitals** | POST | `zoos/1/buildings/1/hospitals/1/lectures/1/visits` | Visit the hospital lecture |
| **Visitors** | DELETE | `zoos/1/visitors/4` | Leave the zoo |

---

## Other API Endpoints

| Resource | HTTP Verb | Resource URL | Use Case |
|---|---|---|---|
| **Visitors** | GET | `zoos/1/visitors` | Get all visitors |
|  | POST | `zoos/1/visitors` | Add a new visitor |
|  | PUT | `zoos/1/visitors/2` | Update visitor personal data |
|  | DELETE | `zoos/1/visitors/4` | Visitor leaves the zoo |
|  | PATCH | `zoos/1/visitors/1` | Update visitor status |
|  | HEAD | `zoos/1/visitors/6` | Check if visitor exists |
| **Tickets** | GET | `zoos/1/tickets` | Get all tickets |
|  | POST | `zoos/1/visitors/4/tickets` | Visitor buys a ticket |
|  | PUT | `zoos/1/visitors/4/tickets/2` | Modify ticket information |
|  | DELETE | `zoos/1/visitors/4/tickets/2` | Delete a visitor's ticket |
|  | PATCH | `zoos/1/visitors/4/tickets/3` | Update ticket (e.g., timestamp) |
|  | HEAD | `zoos/1/visitors/4/tickets/3` | Check if ticket exists |
| **Buildings** | GET | `zoos/1/buildings` | Get all buildings |
|  | POST | `zoos/1/buildings` | Add a building |
| **Shops** | GET | `zoos/1/shops` | Get all shops |
|  | POST | `zoos/1/buildings/1/shops/2/visits` | Visitor visits a shop |
|  | POST | `zoos/1/buildings/1/shops/2/purchases` | Visitor makes a purchase |
| **Hospitals** | POST | `zoos/1/buildings/1/hospitals/1/lecture/1/visits` | Attend a hospital lecture |
| **Enclosures** | GET | `zoos/1/enclosures` | Get all enclosures |
|  | GET | `zoos/1/enclosures/3` | Visit/view a specific enclosure |
| **Animals** | POST | `zoos/1/enclosures/3/animals/2/feeds` | Handler feeds an animal |
|  | POST | `zoos/1/enclosures/3/animals/2/exercises` | Handler exercises an animal |
|  | POST | `zoos/1/enclosures/3/animals/2/examines` | Handler examines an animal |
|  | POST | `zoos/1/hospitals/1/animals/2/heals` | Veterinarian heals an animal |
|  | POST | `zoos/1/hospitals/1/lectures` | Veterinarian lectures |
| **Zoo** | POST | `zoos/1/opens` | Manager opens the zoo |
|  | POST | `zoos/1/closes` | Manager closes the zoo |

