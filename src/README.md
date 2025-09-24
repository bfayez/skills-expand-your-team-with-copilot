# Mergington High School Activities

A comprehensive web application for managing extracurricular activities at Mergington High School. The system provides teachers with tools to manage student registrations and allows easy browsing of activities with advanced filtering capabilities.

## Features

### For Teachers
- **Teacher Authentication** - Secure login system for staff members
- **Student Registration Management** - Sign up and unregister students for activities
- **Real-time Participant Tracking** - View current enrollment numbers for all activities

### For Students & Parents
- **Activity Discovery** - Browse all available extracurricular activities
- **Advanced Filtering** - Filter activities by:
  - Category (sports, academics, arts, etc.)
  - Day of the week (Monday through Sunday)
  - Time of day (Before School, After School, Weekend)
- **Search Functionality** - Quick search through activity names and descriptions
- **Detailed Activity Information** - View schedules, descriptions, and participant counts

### Technical Features
- **FastAPI Backend** - Modern Python web framework with automatic API documentation
- **MongoDB Database** - Flexible data storage for activities and user management
- **Responsive Design** - Mobile-friendly interface that works on all devices
- **Real-time Updates** - Activity lists refresh automatically after changes

## Technology Stack

- **Backend**: Python, FastAPI, PyMongo
- **Database**: MongoDB
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Authentication**: Argon2 password hashing
- **Server**: Uvicorn ASGI server

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional filtering by day and time |
| GET | `/activities/days` | Get list of all days that have activities scheduled |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity (requires teacher auth) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity (requires teacher auth) |
| POST | `/auth/login` | Teacher login endpoint |
| GET | `/auth/check-session` | Validate teacher session |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).

## Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Ensure MongoDB is running on localhost:27017

3. Run the application:
   ```bash
   python -m src.app
   ```

4. Visit http://localhost:8000 to view the application
   - API documentation: http://localhost:8000/docs
