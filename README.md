# Set up JWT authentication and authorization

Secure REST endpoints using JWT and Spring Security.
Handle user registration and authentication.
Note: Always keep your secret keys secure. In production, use environment variables or a secrets manager.

# User Registration (/api/auth/signup): 
  Allows new users to register. The password is encoded using BCryptPasswordEncoder before saving to the database.
# User Authentication (/api/auth/signin): 
  Authenticates the user credentials. If successful, generates and returns a JWT token.
# JWT Token: 
  The token includes the username as the subject and is signed with the secret key.
# Secured Endpoint (/api/test/user): 
  Protected by JWT authentication. Requires a valid JWT token in the Authorization header.
# JWT Validation: 
  The AuthTokenFilter intercepts incoming requests and validates the JWT token. If valid, sets the authentication in the security context.
