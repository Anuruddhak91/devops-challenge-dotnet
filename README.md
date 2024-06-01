# DevOpsChallenge Sales API

## Overview
This project is a Sales API. The application is built using .NET Core and provides functionalities related to sales management.

## Prerequisites
- [.NET 5 SDK](https://dotnet.microsoft.com/download/dotnet/5.0)
- [Docker](https://www.docker.com/products/docker-desktop)
- [Git](https://git-scm.com/)

## Project Setup

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Anuruddhak91/devops-challenge-dotnet.git
    cd DevOpsChallenge.SalesApi
    ```

2. **Restore dependencies**:
    ```bash
    dotnet restore
    ```

3. **Build the project**:
    ```bash
    dotnet build
    ```

4. **Run the project**:
    ```bash
    dotnet run --project src/DevOpsChallenge.SalesApi
    ```

## Running the Application with Docker

1. **Build the Docker image**:
    ```bash
    docker build -t devopschallenge.salesapi .
    ```

2. **Run the Docker container**:
    ```bash
    docker run -d -p 5000:5000 devopschallenge.salesapi
    ```

3. **Access the application**:
    Open your browser and navigate to `http://localhost:5000`.

## Project Structure

```
DevOpsChallenge.SalesApi
├── src
│   ├── DevOpsChallenge.SalesApi
│   ├── DevOpsChallenge.SalesApi.Business
│   └── DevOpsChallenge.SalesApi.Database
└── tests
├── DevOpsChallenge.SalesApi.Business.UnitTests
└── DevOpsChallenge.SalesApi.IntegrationTests
```

- **src/**: Contains the source code of the application.
- **tests/**: Contains unit and integration tests.

## Development

### Adding New Features

1. Create a new branch:
    ```sh
    git checkout -b feature/your-feature-name
    ```

2. Make your changes and commit them:
    ```sh
    git add .
    git commit -m "feat: add your feature"
    ```

3. Push the changes to your branch:
    ```sh
    git push origin feature/your-feature-name
    ```

4. Open a pull request for review.

### Running Tests

To run all unit tests and integration tests:

```bash
dotnet test
```

## Code Style

Please follow the [C# Coding Conventions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions) for this project.

### Conventional Commits

A conventional commit is a standardized commit message format that helps maintain a clear project history and automates the versioning process.

### Commit Message Format

Each commit message should consist of a header, an optional body, and an optional footer. The header has a special format that includes a type, an optional scope, and a subject:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

### Types

- feat: A new feature for the user.
- fix: A bug fix for the user.
- docs: Documentation only changes.
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
- refactor: A code change that neither fixes a bug nor adds a feature.
- perf: A code change that improves performance.
- test: Adding missing tests or correcting existing tests.
- chore: Changes to the build process or auxiliary tools and libraries such as documentation generation.

### Examples

Example 1: Adding a new feature

```
feat(user): add ability to view user profile
```

Example 2: Fixing a bug

```
Example 2: Fixing a bug
```

Example 3: Documentation update

```
docs(readme): update setup instructions
```
