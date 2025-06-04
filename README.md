# Event Management API 🎉

This is a full-featured server-side project built with **ASP.NET Core** and **SQL Server**, allowing users to manage events, register participants, and view weather forecasts for event locations.

## 📌 Features

- ✅ Create, read, update, and delete events
- ✅ Register users to events
- ✅ Get all users registered to an event
- ✅ Get a list of all upcoming events
- ✅ Get real-time weather for event locations (via OpenWeatherMap API)
- ✅ In-memory caching for weather requests
- ✅ Seeded database on startup
- ✅ Full Postman Collection for testing

## 🛠 Technologies

- ASP.NET Core Web API
- Entity Framework Core
- SQL Server
- Swagger (OpenAPI)
- Postman
- C#
- OpenWeatherMap API

## 📁 Project Structure

EventManagement/
├── Controllers/
│ └── EventsController.cs
├── Data/
│ └── EventsDbContext.cs
├── Dtos/
│ ├── EventCreateDto.cs
│ └── UserCreateDto.cs
├── Models/
│ ├── Event.cs
│ ├── EventUser.cs
│ └── User.cs
├── Postman Collection/
│ └── EventManagementAPI.postman_collection.json
├── SQL Script/
│ └── SeedData.sql
├── wwwroot/
│ └── events.yaml
├── Properties/
│ └── launchSettings.json
├── appsettings.json
├── Program.cs
├── EventManagement.sln


---

## 🔄 Database Setup

Upon starting the application, the following happens:

- The existing database is **dropped and recreated**
- Data is **seeded automatically** from the file:



💡 **If you unzip the project and open it manually**, make sure to **run the SQL script manually** before testing if automatic seeding is disabled or fails.

---

## 🌐 API Endpoints

| Method | Route                                  | Description                             |
|--------|----------------------------------------|-----------------------------------------|
| GET    | `/schedule`                            | Get all scheduled events                |
| POST   | `/api/events`                          | Create a new event                      |
| GET    | `/api/events/{id}`                     | Get event by ID                         |
| PUT    | `/api/events/{id}`                     | Update event                            |
| DELETE | `/api/events/{id}`                     | Delete event                            |
| POST   | `/api/events/{id}/registration`        | Register user to event                  |
| GET    | `/api/events/{id}/registration`        | Get registered users for an event       |
| GET    | `/api/events/{id}/weather`             | Get weather forecast for event location |

---

## 🧪 Postman Collection

- A ready-made Postman collection is included here:
Postman Collection/EventManagementAPI.postman_collection.json


To use it:
1. Open Postman
2. Click **Import**
3. Select the `.json` file
4. Make sure your backend is running on: https://localhost:7286


Use the sample requests provided in the collection to test all endpoints.

---

## 🔐 API Key for Weather

This project uses OpenWeatherMap API for weather data.  
The API key is already embedded: cb4169250b44e87579b7829b1bc3b134

You may replace this key in `EventsController.cs` if needed.

---

## 🧳 Getting Started (Quick Summary)

1. Clone or unzip the project folder.
2. Open the `.sln` file in Visual Studio.
3. Make sure SQL Server is running.
4. Optionally, run the SQL script in `SQL Script/SeedData.sql` manually.
5. Run the app (`IIS Express` or project profile).
6. Import the Postman collection.
7. Test endpoints via Postman or Swagger (`https://localhost:7286/swagger`).

---

## 🧾 License

This project was developed as part of a university assignment. You are free to use or adapt it with attribution.




