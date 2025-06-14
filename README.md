# 🎉 Event Management API

A full-featured event management system built with **ASP.NET Core**, **SQL Server**, and a custom **HTML/JS frontend**. It allows users to create, manage, and register for events — with live validations and weather forecast integration.

---

## 📌 Features

- ✅ Create, read, update, and delete events
- ✅ User registration to events with duplicate check
- ✅ Auto-decrement of available event slots (`MaxRegistrations`)
- ✅ View a public schedule of upcoming events
- ✅ Google Maps integration for event location
- ✅ Real-time weather forecast using OpenWeatherMap API
- ✅ Caching to reduce redundant weather calls
- ✅ Responsive front-end with validation logic
- ✅ Postman Collection for all endpoints
- ✅ SQL script for full DB creation and seeding

---

## 🛠 Technologies

- ASP.NET Core Web API
- Entity Framework Core
- SQL Server
- JavaScript + HTML + CSS
- OpenWeatherMap API
- Postman
- Swagger
- Visual Studio 2022

---

## 📁 Project Structure

EventManagement/
├── Controllers/
│ ├── EventsController.cs
│ └── UsersController.cs
├── Data/
│ └── EventsDbContext.cs
├── Dtos/
│ ├── EventCreateDto.cs
│ └── UserCreateDto.cs
├── Models/
│ ├── Event.cs
│ ├── EventUser.cs
│ └── User.cs
├── wwwroot/
│ ├── index.html
│ ├── style.css
│ └── app.js
├── SQL Script/
│ └── Events.sql
├── Postman/
│ └── EventManagement_API_Collection.postman_collection.json
├── Program.cs
├── appsettings.json
└── EventManagement.sln

yaml
Copy
Edit

---

## 🌐 API Endpoints

| Method | Route                                  | Description                             |
|--------|----------------------------------------|-----------------------------------------|
| GET    | `/schedule`                            | Get all upcoming events                 |
| POST   | `/api/events`                          | Create a new event                      |
| GET    | `/api/events/{id}`                     | Get event by ID                         |
| PUT    | `/api/events/{id}`                     | Update event                            |
| DELETE | `/api/events/{id}`                     | Delete event                            |
| POST   | `/api/events/{id}/registration`        | Register user to event (via user name)  |
| GET    | `/api/events/{id}/registration`        | Get all users registered to an event    |
| GET    | `/api/users/name/{name}`               | Get user by name                        |
| GET    | `/api/events/{id}/weather`             | Get weather forecast for event location |

---

## 🧪 Postman Collection

The full Postman collection is provided under:

Postman/EventManagement_API_Collection.postman_collection.json

yaml
Copy
Edit

To use:
1. Open Postman
2. Click **Import** → Select `.json` file
3. Test endpoints on `https://localhost:7286`

---

## 🗺️ Google Maps Integration

Each event includes a “Map” button that opens the event’s location in **Google Maps**, based on its `Location` string. This satisfies the “extra functionality” requirement for full project credit.

---

## 🔐 Weather API Key

The project uses OpenWeatherMap API with the key:

cb4169250b44e87579b7829b1bc3b134

yaml
Copy
Edit

You can change it in `EventsController.cs`.

---

## 🧳 Getting Started

1. Clone or unzip the repository.
2. Open `EventManagement.sln` in Visual Studio 2022.
3. Ensure SQL Server is running.
4. Optional: run `SQL Script/Events.sql` to manually seed data.
5. Press F5 or run the project profile to start the backend.
6. Open `wwwroot/index.html` in a browser to access the frontend.
7. Use Swagger (`/swagger`) or Postman to test the API.

---

## 🧾 License

This project was developed as part of a university assignment.  
You may reuse or adapt this code with proper attribution.

---

## 👨‍💻 Author

Tysier Zidan
