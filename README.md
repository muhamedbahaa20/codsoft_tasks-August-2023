### Schedule App Endpoints Table

| Name                        | Method           | Body                                                         | Response                                                                                                  | Steps                                                                                                                 | Expected Result                                                                                                               |
|-----------------------------|------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| List & Create Schedule      | GET, POST        | GET: None<br>POST: `{"title": "string", "date": "datetime"}` | GET: 200 OK, List of schedules<br>POST: 201 Created, Schedule object                                       | 1. Send GET or POST request <br>2. For POST, include schedule data in the body <br>3. For GET, fetch list of schedules | GET request returns a list of schedules. POST request creates a new schedule and returns the created schedule object.       |
| Retrieve, Update & Delete Schedule | GET, PUT, PATCH, DELETE | GET: None<br>PUT/PATCH: `{"title": "string", "date": "datetime"}`<br>DELETE: None | GET: 200 OK, Schedule object<br>PUT/PATCH: 200 OK, Updated schedule object<br>DELETE: 204 No Content       | 1. Send GET, PUT, PATCH, or DELETE request with schedule ID <br>2. For PUT/PATCH, include updated data in the body <br>3. Perform action | GET request returns the schedule object. PUT/PATCH request updates the schedule and returns the updated object. DELETE request removes the schedule. |
| List & Create Task          | GET, POST        | GET: None<br>POST: `{"title": "string", "description": "string", "due_date": "datetime"}` | GET: 200 OK, List of tasks<br>POST: 201 Created, Task object                                              | 1. Send GET or POST request with schedule ID <br>2. For POST, include task data in the body <br>3. For GET, fetch list of tasks | GET request returns a list of tasks in the specified schedule. POST request creates a new task and returns the created task object. |
| Retrieve, Update & Delete Task | GET, PUT, PATCH, DELETE | GET: None<br>PUT/PATCH: `{"title": "string", "description": "string", "due_date": "datetime"}`<br>DELETE: None | GET: 200 OK, Task object<br>PUT/PATCH: 200 OK, Updated task object<br>DELETE: 204 No Content | 1. Send GET, PUT, PATCH, or DELETE request with schedule ID and task ID <br>2. For PUT/PATCH, include updated data in the body <br>3. Perform action | GET request returns the task object. PUT/PATCH request updates the task and returns the updated object. DELETE request removes the task. |
| List All Schedules & Tasks  | GET              | None                                                         | 200 OK, List of schedules with their associated tasks                                                     | 1. Send GET request                                                                                                        | GET request returns a list of schedules with their associated tasks.                                                      |
