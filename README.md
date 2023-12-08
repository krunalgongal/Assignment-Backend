Task API Documentation

## Create Task

### Endpoint


POST /tasks


### Description

Create a new task.

### Request Body

json
{
  "title": "Task Title",
  "description": "Task Description"
}


### Response

json
{
  "Message": "Task creation successful",
  "task": {
    "id": "uniqueId",
    "title": "Task Title",
    "description": "Task Description"
  }
}


## Read All Tasks

### Endpoint


GET /tasks


### Description

Retrieve a list of all tasks.

### Response

json
{
  "Message": "List of all tasks",
  "Tasks": [
    {
      "id": "uniqueId1",
      "title": "Task Title 1",
      "description": "Task Description 1"
    },
    {
      "id": "uniqueId2",
      "title": "Task Title 2",
      "description": "Task Description 2"
    },
    // ... other tasks
  ]
}


## Read One Task

### Endpoint


GET /tasks/:id


### Description

Retrieve details of a specific task.

### Response

json
{
  "id": "uniqueId",
  "title": "Task Title",
  "description": "Task Description"
}


### Error Response

json
{
  "error": "Task not found"
}


## Update Task

### Endpoint


PUT /tasks/:id


### Description

Update details of a specific task.

### Request Body

json
{
  "title": "Updated Task Title",
  "description": "Updated Task Description"
}


### Response

json
{
  "id": "uniqueId",
  "title": "Updated Task Title",
  "description": "Updated Task Description"
}


### Error Response

json
{
  "error": "Task not found"
}


## Delete Task

### Endpoint


DELETE /tasks/:id


### Description

Delete a specific task.

### Response

json
{
  "Message": "Deleted Task",
  "ListTask": [
    // ... remaining tasks after deletion
  ]
}


### Error Response

json
{
  "error": "Task not found"
}