# Django PostgreSQL Project

This is a Django project template with PostgreSQL database integration using Docker.

## Prerequisites

Before you can run this project, make sure you have the following installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)

## Getting Started

Follow these steps to set up and run the project:

1. Clone the repository or download the source code:

   ```shell
   git clone git@github.com:sbstnzcr/docker-django-postgresql.git
   ```

2. Navigate to the project directory:

   ```shell
   cd docker-django-postgresql
   ```

3. Start the Docker containers:

   ```shell
   docker-compose up --build
   ```

4. Access the Django development server:

   Open your web browser and visit [http://localhost:8000](http://localhost:8000). You should see the default Django landing page.

## Configuration

The project is pre-configured to use PostgreSQL as the database. The configuration can be found in the `config/settings.py` file. Update the `DATABASES` setting with your PostgreSQL database credentials.

By default, the PostgreSQL container is configured with the following environment variables:

- `POSTGRES_DB`: The name of the database.
- `POSTGRES_USER`: The username to connect to the database.
- `POSTGRES_PASSWORD`: The password for the database user.

## Database Migrations

To apply database migrations, run the following command:

```shell
docker-compose run web python manage.py migrate
```

This will create the necessary database tables.

## Development

You can start developing your Django application by editing the project files located in the `config` directory. The `manage.py` script is used to run various management commands.

To stop the Docker containers, use `Ctrl + C` in the terminal where they are running.

## Deployment

This project template is primarily intended for local development. For production deployment, you will need to configure additional settings, such as a production-ready web server and proper database configuration.

Refer to the [Django documentation](https://docs.djangoproject.com/) for more information on deploying Django applications.

## Contributing

Contributions are welcome! If you find any issues or would like to suggest improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).