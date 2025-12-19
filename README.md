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

### Django Build the Docker image
<img width="1342" height="757" alt="Django build log" src="https://github.com/user-attachments/assets/cfc7f205-22f8-48f5-8390-dbbebc93249b" />

### Django Run the container
<img width="1340" height="754" alt="Django container run" src="https://github.com/user-attachments/assets/b9e2b5be-8a0e-46ea-96ee-1ba8946b53ef" />

### Django verify the container status and Image
<img width="1337" height="754" alt="Django image" src="https://github.com/user-attachments/assets/b840dba9-0c38-4771-851f-9f1712ae0b58" />





### Application Access

| Service            | URL                                                          |
| ------------------ | ------------------------------------------------------------ |
| Django Application | [http://localhost:8000](http://localhost:8000)               |
| Demo Page          | [http://localhost:8000/demo/](http://localhost:8000/demo/)   |
| Django Admin       | [http://localhost:8000/admin/](http://localhost:8000/admin/) |

### Django Demo Page
<img width="1268" height="758" alt="Django werbpage URL" src="https://github.com/user-attachments/assets/bf0d2b27-ba8f-457a-ba44-66ebb22d5988" />

### Django Admin Page
<img width="1304" height="776" alt="Django webpage ADmin" src="https://github.com/user-attachments/assets/04dae6ef-d941-40ed-a79a-5fa00487291f" />



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
