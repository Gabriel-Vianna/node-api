API Pet-Shop<br>
<br>
API built on NodeJS using Express framework and MySQL database.<br>
The goal is to provide a scheduling and consultation API in a pet shop.

After cloning the repository, follow the steps to install the dependencies and launch the application, you must have NodeJS previously installed on the computer.

$ cd pet-shop<br>
$ npm install<br>
$ npm start<br>
<br>
<br>
API Response Routes:
<br>
List records<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos<br>
Method HTTP: GET<br>
Response: Returns a JSON object with all scheduled services in the database.<br>
<br>
<br>
Create record<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos<br>
Method HTTP: POST<br>
Response: Sends a request to the server with the fields required to schedule a new service, if the request succeeds, the created JSON object is returned.<br>

Required fields for requisition:

-> cliente: String with the client name<br>
-> pet: String with the pet name<br>
-> servico: String with the name of the service to be scheduled in the pet shop<br>
-> status: String with service status (Scheduled/Canceled/Delayed ...)<br>
-> observacoes: String with remarks about the animal<br>
-> data: Date in DD/MM/YYYY format, informing the service date<br>
<br>
<br>
Search by ID<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
Method HTTP: GET<br>
Response: Returns a JSON object associated with the ID passed in the request url.<br>
<br>
<br>
Delete record<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
Method HTTP: DELETE<br>
Response: Deletes the record associated with the ID passed as a parameter.<br>
<br>
<br>
Edit record<br>
<br>
-> Endpoint: http://localhost:3000/atendimentos/id<br>
Method HTTP: PATCH<br>
Response: Send a request to the server passing in the body the fields to be edited in an existing record, must be passed the record id in the request url.<br>
<br>
<br>