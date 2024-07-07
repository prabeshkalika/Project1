
# Python API Server

This is a simple Python API Server using POST to save data to MongoDB and GET requests to receive the data from MongoDB.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Python 3.6 or higher.
- You have a basic understanding of Python projects and virtual environments.

## Installation

### Setting Up a Virtual Environment

To avoid conflicts with other Python projects you may be working on, it's a good idea to use a virtual environment. Here's how you can set one up:

**For Windows:**

```cmd
python -m venv venv
.\venv\Scripts\activate
```

### Installing Dependencies

Once your virtual environment is activated, install the project dependencies by running:

```bash
pip install -r requirements.txt
```
## Create a Docker network to facilitate communication between your Python application container and a MongoDB container.

## Replace with a name of your choice:
```bash
docker network create mynetwork
```
## Run Your Python Application Container
## Run your Docker image as a container within the same Docker network. Ensure it can successfully communicate with the MongoDB container
```bash
docker run --network mynetwork -d -p 3000:3000 --name assignment1 prabeshkalika/assignment1:version1
```
## Ensure your MongoDB instance is running and accessible as configured in your Python script.
```bash
docker run --network mynetwork --name mongodb -d -p 27017:27017 -v my_mongo_data:/data/db mongo:latest
```


## Using the Application

To interact with the application, you can use the following `curl` command to create a new item in the database:

```bash
curl -X POST http://localhost:3000/items \
     -H "Content-Type: application/json" \
     -d '{"id": "4", "name": "maziar"}'
```  
## Contributing to the Project

Contributions to enhance the project are welcome. Please fork the repository and create a pull request.

## License

This project is licensed under the GPLv3.

---

"# Assignment1" 
