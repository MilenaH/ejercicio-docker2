# Copilot Instructions for AI Agents

## Project Overview
This is a minimal Python application designed to run inside a Docker container. The main script (`app.py`) prints a greeting message. The project is structured for simplicity and educational purposes.

## Key Files
- `app.py`: Main Python script. Prints "Hola Ecuador" when executed.
- `Dockerfile`: Defines the build for a minimal Python 3.14 Alpine-based container. Copies `app.py` and sets it as the entrypoint.
- `README.md`: (Currently empty) Add project documentation here if needed.

## Build & Run Workflow
- **Build Docker Image:**
  ```sh
  docker build -t ejercicio-docker .
  ```
- **Run Container:**
  ```sh
  docker run --rm ejercicio-docker
  ```
- The container will output: `Hola Ecuador`

## Conventions & Patterns
- All application logic is in `app.py`.
- No external dependencies or requirements files are used.
- The Dockerfile uses `CMD ["python", "app.py"]` for execution.
- No tests or CI/CD are present; add as needed for future expansion.

## Agent Guidance
- When adding features, keep the structure minimal and update the Dockerfile if new dependencies are introduced.
- Document any new workflows or commands in the `README.md`.
- Follow the existing pattern: all logic in `app.py`, containerized via Docker.

## Example: Adding a Dependency
If you add a package, update the Dockerfile:
```dockerfile
RUN pip install <package>
```

---
For questions or unclear conventions, ask for clarification or propose updates here.
