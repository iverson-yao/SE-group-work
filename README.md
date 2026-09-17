# Multimodal In-Vehicle Interaction System

Team software engineering project integrating speech, gesture, and computer-vision modules into a Flask-based vehicle interaction platform.

**Tech Stack:** Python · Flask · SQLite · MediaPipe · HTML/CSS · JavaScript

**Highlights**
- Unified independently developed speech, gesture, and vision modules behind a common application workflow.
- Added authentication, vehicle-state controls, driver-safety alerts, interaction logging, and a browser-based control interface.
- My primary focus was system architecture, module interfaces, end-to-end integration, and cross-module debugging.

## Overview

The system provides a web interface for multimodal vehicle interaction. User inputs are routed through independently developed recognition modules, combined with vehicle-state logic, and surfaced through application controls and safety alerts. Interaction history is recorded in SQLite for later review.

This repository is a cleaned public mirror for portfolio and resume review. The original project was completed as a team course project, and GitHub commit history may not fully reflect each teammate's work because parts of the collaboration happened through file exchange and offline coordination.

## Architecture

- **Backend:** Flask application with route modules for authentication and system control.
- **Database:** SQLite schema for users and interaction logs.
- **Gesture module:** MediaPipe-based gesture recognition wrapper and integration interface.
- **Vision module:** Driver distraction and fatigue detection integration.
- **Voice module:** Voice interaction integration.
- **Frontend:** HTML templates, CSS, and JavaScript for login, registration, controls, and log views.

## Key Components

- `app.py`: Flask application setup, session configuration, blueprint registration, and database initialization.
- `modules/auth.py`: Login, registration, logout, password verification, and optional face-login flow.
- `modules/system.py`: Core control routes, multimodal module orchestration, vehicle-state updates, alerts, and log refresh endpoints.
- `db_schema.py` and `db_utils.py`: SQLite schema creation and helper functions for users and interaction logs.
- `gesture.py`, `visual.py`, `voice.py`: Integration-facing wrappers for recognition modules.
- `templates/` and `static/`: Web UI templates and browser-side assets.

## My Contributions

- Designed the system architecture and module interfaces for a multimodal vehicle interaction platform, enabling parallel development of speech, gesture, and vision components.
- Integrated independently developed modules into an end-to-end Flask application with vehicle-state controls, driver-safety alerts, interaction logging, and a web control interface.
- Led system-level debugging and demo validation, identifying cross-module runtime failures and coordinating iterative fixes across component owners.

## Team Scope

This was a team project. Individual recognition models and some component-level implementations were developed by different teammates. The contribution statements above describe the system architecture, integration, and debugging work I personally focused on.

## Running Locally

Install the dependencies listed in `requirements.txt`, then run:

```bash
python app.py
```

Some recognition modules depend on model files or local runtime resources that may not be included in this public mirror. The Flask application structure, integration interfaces, and control flow can still be reviewed independently.
