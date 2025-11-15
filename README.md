COMMUNICATION CONTRACT

---Requesting Data---
- file: crud_requests.json
- format: JSON array of request objects
  -    [
        {
          'command': 'COMMAND_NAME_', 
          "data": { ... }
        }
  ]

- Commands and Data
  - CREATE - provide item to create, including its 'id' and other data fields
  - RETRIEVE - include 'id' to retrieve single item or leave blank to get all items
  - UPDATE - provide 'id' of item to update and 'updates' dictionary containing fields and their new values
  - DELETE - provide the 'id' of item to be deleted

- Example Request Call -
[
  {
    'command': 'CREATE',
    'data': {
      'id': '1',
      'habit': '1000 push ups',
      'frequency': '1',
      'period': 'day'
    }
  }
]


---Receiving Data---
  - file: crud_responses.json
  - format: JSON array of response objects
  - generally includes status indicator, message, and object item of request
  
- Example Response Call -
[
  {
    'status': 'success',
    'message': 'Item 1 was successfully created!',
    'item': {
      'id': '1',
      'habit': '1000 push ups',
      'frequency': '1',
      'period': 'day'
    }
  }
]


*** UML DIAGRAM TO BE ADDED ***
  
