# Todo List Backend

This repository contains the backend for the Todo List application, built with **Ruby on Rails**. It provides the API endpoints necessary for managing tasks and integrates seamlessly with the [frontend repository](https://github.com/Btojaka/frontend_git), which is developed using React JS.

## Key Features

- RESTful API for task management (create, read, update, delete).
- Data persistence using a **PostgreSQL** database.
- Secure and structured backend logic with Rails conventions.
- JSON responses for easy integration with frontend.

## Prerequisites

Before starting, ensure you have the following installed:

- [Ruby](https://www.ruby-lang.org/) (version 3.0.0 or higher).
- [Ruby on Rails](https://rubyonrails.org/) (version 7.0 or higher).
- [PostgreSQL](https://www.postgresql.org/).
- [Bundler](https://bundler.io/) for dependency management.

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/Btojaka/react_rails_todo.git
   cd react_rails_todo
   ```

2. Install dependencies:

   ```bash
   bundle install
   ```

3. Set up the database:

   ```bash
   rails db:create
   rails db:migrate
   ```

4. Start the Rails server:
   ```bash
   rails server
   ```

The server will start at `http://localhost:3000` by default.

## API Endpoints

| Method | Endpoint            | Description            |
| ------ | ------------------- | ---------------------- |
| GET    | `/api/v1/todos`     | Fetch all tasks        |
| POST   | `/api/v1/todos`     | Create a new task      |
| GET    | `/api/v1/todos/:id` | Fetch a specific task  |
| PATCH  | `/api/v1/todos/:id` | Update a specific task |
| DELETE | `/api/v1/todos/:id` | Delete a specific task |

## Project Structure

```plaintext
app/
├── controllers/
│   └── api/
│       └── todos_controller.rb  # Handles API requests for tasks
├── models/
│   ├── todo.rb                  # Task model
│   └── application_record.rb    # Base model class
├── views/                       # Unused (API only)
├── jobs/                        # Background jobs (if applicable)
├── mailers/                     # Mailer logic (not used)
├── channels/                    # WebSocket channels (not used)
└── concerns/                    # Reusable modules

config/
├── routes.rb                    # Defines API routes
└── database.yml                 # Database configuration

db/
├── migrate/                     # Database migrations
└── schema.rb                    # Database schema

```

## Technologies Used

- **Ruby on Rails**: Web application framework.
- **PostgreSQL**: Database for storing tasks.
- **RSpec**: For testing (if tests are implemented).

## Contributing

Contributions are welcome! Follow these steps:

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/new-feature`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push your branch (`git push origin feature/new-feature`).
5. Open a Pull Request.

## License

This project is licensed under the [MIT License](LICENSE).

## Useful Links

- [Frontend Repository](https://github.com/Btojaka/frontend_git)
- [Ruby on Rails Documentation](https://guides.rubyonrails.org/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

---

Thank you for contributing or using this application! If you have any questions, feel free to open an issue.
