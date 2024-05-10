# Gateway Configuration

The Gateway acts as the central entry point for all incoming requests to the microservices in our social networking platform. It maps external API calls to the appropriate internal microservices.

## Routes Configuration

Below are the configured routes in the Gateway, which enable the redirection of incoming requests to the correct microservice based on the path and method of the request:

### User Service Routes

1. **Register User**
   - **External Path:** `/auth/register`
   - **Method:** POST
   - **Internal Path:** `/user-service/auth/register`
   - **Service Host:** `userservice:8080`

2. **Login User**
   - **External Path:** `/auth/login`
   - **Method:** POST
   - **Internal Path:** `/user-service/auth/login`
   - **Service Host:** `userservice:8080`

3. **Follow User**
   - **External Path:** `/follow`
   - **Method:** POST
   - **Internal Path:** `/user-service/follow`
   - **Service Host:** `userservice:8080`

4. **Search Users**
   - **External Path:** `/search`
   - **Method:** GET
   - **Internal Path:** `/user-service/search`
   - **Service Host:** `userservice:8080`

### Feed Service Routes

1. **User Feed**
   - **External Path:** `/feed`
   - **Method:** GET
   - **Internal Path:** `/feed`
   - **Service Host:** `feedservice:8080`

### Post Service Routes

1. **Create Post**
   - **External Path:** `/post`
   - **Method:** POST
   - **Internal Path:** `/post`
   - **Service Host:** `postservice:8080`

2. **Retrieve Post**
   - **External Path:** `/post`
   - **Method:** GET
   - **Internal Path:** `/post`
   - **Service Host:** `postservice:8080`

3. **Retrieve Specific Post**
   - **External Path:** `/post/{id}`
   - **Method:** GET
   - **Internal Path:** `/post/{id}`
   - **Service Host:** `postservice:8080`

4. **Retrieve All Posts**
   - **External Path:** `/post/all`
   - **Method:** GET
   - **Internal Path:** `/post/all`
   - **Service Host:** `postservice:8080`
