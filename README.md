# AuditTracker

A plug-and-play .NET Core (8.0) Audit & Compliance Tracker. Easily log and query database changes and manual events.

## Features
- Intercepts EF Core changes
- Tracks Create, Update, Delete operations
- Manual custom event logging
- API to query audit logs
- Uses in-memory DB (change to SQL Server in production)

## Getting Started

1. Clone the repo
2. Run with `dotnet run`
3. Access Swagger UI at `/swagger`

## To Use with SQL Server

Replace this line in `Program.cs`:
```
options.UseInMemoryDatabase("AuditDb");
```
With:
```
options.UseSqlServer(builder.Configuration.GetConnectionString("Default"));
```

And configure your connection string in `appsettings.json`.

## License

MIT