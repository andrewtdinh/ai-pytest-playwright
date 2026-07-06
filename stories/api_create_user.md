Title: Create user - authenticated POST with payload

Type: api
Base URL: https://reqres.in

As a consumer of the Users API, I want to authenticate and then create a new user so I can verify the full auth + write flow.

Acceptance criteria:
- Send POST /api/login with JSON body {"email": "eve.holt@reqres.in", "password": "cityslicka"}
- Expect login status code 200
- Expect login response body to contain field "token" with a non-empty string value
- Extract the token from the login response
- Send POST /api/users with header "Authorization: Bearer {token}" and JSON body {"name": "morpheus", "job": "leader"}
- Expect create status code 201
- Expect "Content-Type" header to include "application/json"
- Expect response body to contain field "name" with value "morpheus"
- Expect response body to contain field "job" with value "leader"
- Expect response body to contain field "id" with a non-empty string value
- Expect response body to contain field "createdAt" with a non-empty string value
