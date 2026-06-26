Title: Get user by ID - valid ID

Type: api
Base URL: https://jsonplaceholder.typicode.com

As a consumer of the Users API, I want to fetch a single user by their ID so I can display their profile.

Acceptance criteria:
- Send GET /users/1
- Expect status code 200
- Expect response body to contain field "id" with value 1
- Expect response body to contain field "name" with value "Leanne Graham"
- Expect response body to contain field "email"
- Expect response body to contain nested field "address" with a "city" key
- Expect "Content-Type" header to include "application/json"
