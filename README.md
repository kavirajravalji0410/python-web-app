# Django Web Application using Docker
This repository contains a simple Django web application running inside a Docker container.

The goal of this project is to understand how a Django application can be containerized and executed without installing Python or Django on the host system.

This setup is meant for learning and local testing, not for production use.

## Purpose of this Project

- Practice Docker image creation using a Dockerfile
- Run a Django application inside a container
- Expose the application using Docker port mapping
- Verify Django Admin and application routes
- Understand basic Docker commands used during development

## Tech Stack
- Python
- Django
- Docker
- Ubuntu (container base image)


## Project Structure
```
python-web-app/
├── devops/
│   ├── demo/              # Django app
│   ├── devops/            # Django project settings
│   ├── manage.py
│   └── db.sqlite3
├── Dockerfile
├── requirements.txt
└── README.md
```
## Prerequisites
Make sure the following tools are installed:
- Docker Desktop
- Git

No Python or Django installation is required on the local machine.

## How to Run the Application
### Step 1: Clone the repository
```
git clone https://github.com/kavirajravalji0410/python-web-app.git
cd python-web-app
```
### Step 2: Build the Docker image
``` 
docker build -t django . 
```
### Step 3: Run the container
```
docker run -d -p 8000:8000 django
```
### Step 4: Verify container status
```
docker ps
```
You should see the Django container running with port 8000 exposed.

### Application Access

| Service            | URL                                                          |
| ------------------ | ------------------------------------------------------------ |
| Django Application | [http://localhost:8000](http://localhost:8000)               |
| Demo Page          | [http://localhost:8000/demo/](http://localhost:8000/demo/)   |
| Django Admin       | [http://localhost:8000/admin/](http://localhost:8000/admin/) |

### About the Admin Page
If you open:
```
http://localhost:8000/admin/
```
You will see the Django admin login screen.

Seeing this page confirms:

- Django server is running
- Container networking is working
- Port mapping is correctly configured

### Useful Docker Commands
```
docker images
docker ps
docker logs <container_id>
docker stop <container_id>
```
### Author

Kaviraj Ravalji

DevOps Engineer

GitHub: https://github.com/kavirajravalji0410

Medium: https://medium.com/@kavirajravalji2022

### Final Remarks

This project helped in understanding:

- Django application structure
- Docker image creation
- Running and debugging containers
- Basic Docker workflows used in real projects

Feel free to fork or use this repository as a reference.
