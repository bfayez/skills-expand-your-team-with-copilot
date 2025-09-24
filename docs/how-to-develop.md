# Development Guide

## Initial Setup

This project is best developed using GitHub Codespaces, which provides a consistent development environment with all the necessary tools pre-configured.

### Setting up your development environment

1. Open the repository in a codespace
2. Wait for the container to finish building and installing dependencies
3. Install Python dependencies by running:

   ```bash
   python -m pip install -r requirements.txt
   ```

### Dependencies

The project requires the following Python packages:

- FastAPI - Modern web framework for building APIs
- Uvicorn - ASGI server implementation for running the FastAPI application

These dependencies will be installed when you run `pip install -r requirements.txt`

## Debugging

### Running the website locally

1. From VS Code's Run and Debug view (Ctrl+Shift+D), select "Launch Mergington WebApp" from the launch configuration dropdown
2. Press F5 or click the green play button to start debugging
3. The website will be available at `http://localhost:8000`
4. The API documentation will be available at `http://localhost:8000/docs`

### Debugging tips

- FastAPI's auto-reload feature will automatically restart the server when you make code changes
- Use the interactive API documentation at `/docs` to test your endpoints

## Getting Started

1. Install the dependencies:

   ```bash
   pip install fastapi uvicorn
   ```

2. Run the application:

   ```bash
   python app.py
   ```

3. Open your browser and go to:
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## Usage

### API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with their details and current participant count |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up for an activity                                             |

> [!IMPORTANT]
> All data is stored in memory, which means data will be reset when the server restarts.

## Teacher Support

### Issue Templates

This repository includes comprehensive issue templates designed to help teachers request changes and improvements without needing to modify code directly. These templates are located in `.github/ISSUE_TEMPLATE/` and include:

- **Bug Report** - For system problems and errors
- **Feature Request** - For new functionality requests  
- **Activity Management** - For activity-related changes (schedules, registrations, etc.)
- **UI/UX Improvement** - For interface and experience improvements
- **Data & Content Update** - For content and information updates
- **Security & Access** - For security issues and access control
- **General Request** - For other requests not covered above

Each template is designed to provide Copilot coding agents with sufficient context to implement changes without additional clarification.

### Using Issue Templates

Teachers can access these templates by:

1. Going to the [Issues page](../issues)
2. Clicking "New Issue" 
3. Selecting the appropriate template
4. Filling out all required fields with detailed information
5. Submitting the issue

See the [Issue Template README](../.github/ISSUE_TEMPLATE/README.md) for detailed guidance on using each template.
