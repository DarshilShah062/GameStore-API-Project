# GameStore API Project

A .NET Core Web API project for managing video games, built with Entity Framework Core and SQLite.

## 📋 Project Overview

This project implements a RESTful API for a game store with the following features:
- CRUD operations for games
- SQLite database integration
- Entity Framework Core
- Clean architecture

## 🚀 Getting Started

### Prerequisites
- .NET 9.0 SDK
- Visual Studio Code or Visual Studio 2022
- SQLite browser (optional)

### Installation

1. **Clone the repository**
```bash
git clone [repository-url]
cd GameStore
```

2. **Install dependencies**
```bash
dotnet restore
```

3. **Set up the database**
```bash
dotnet ef database update
```

4. **Run the application**
```bash
dotnet run
```

## 🔌 API Endpoints

### Games

```http
# Get all games
GET https://localhost:7170/games

# Get a specific game
GET https://localhost:7170/games/{id}

# Create a new game
POST https://localhost:7170/games
Content-Type: application/json

{
    "title": "Game Title",
    "genre": "Action",
    "price": 59.99,
    "releaseDate": "2024-01-01"
}

# Update a game
PUT https://localhost:7170/games/{id}
Content-Type: application/json

{
    "title": "Updated Title",
    "genre": "Adventure",
    "price": 49.99,
    "releaseDate": "2024-01-01"
}

# Delete a game
DELETE https://localhost:7170/games/{id}
```

## 🗄️ Project Structure

```
GameStore/
├── Data/
│   ├── DBContext.cs
│   └── Migrations/
├── DTOs/
│   ├── GameDto.cs
│   ├── CreateGameDto.cs
│   └── UpdateGameDto.cs
├── Entities/
│   ├── Game.cs
│   └── Genre.cs
├── EndPoints/
│   └── GamesEndPoints.cs
└── Program.cs
```

## 🛠️ Development

To run the project in development mode:

```bash
dotnet watch run
```

### Database Migrations

Create a new migration:
```bash
dotnet ef migrations add [MigrationName]
```

Apply migrations:
```bash
dotnet ef database update
```

## 📚 Technologies Used

- ASP.NET Core 9.0
- Entity Framework Core
- SQLite
- C# 12

## 🌟 Features

- Full CRUD operations for games
- Database persistence
- Error handling
- DTOs for data transfer
- Clean architecture principles
- Entity Framework Core integration

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🏃‍♂️ Running Tests

```bash
dotnet test
```

## 🔍 Troubleshooting

If you encounter the SSL/TLS error, try:
1. Trust the development certificate:
```bash
dotnet dev-certs https --trust
```
2. Use the correct URL (https://localhost:7170)

For any other issues, please check the [issues](https://github.com/yourusername/GameStore/issues) page.
