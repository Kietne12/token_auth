# Test token_auth

1. Go to profile  
GET http://localhost:3000/api/auth/profile  
![Profile No Token](public/results/profile_no_token.png)

2. Register  
POST http://localhost:3000/api/auth/register  
Body
{
  "username": "thekiet",
  "email": "thekiet@example.com",
  "password": "12345"
}  
![Register Success](public/results/register.png)


3. Login  
POST http://localhost:3000/api/auth/login  
Body
{
  "email": "thekiet@example.com",
  "password": "12345"
}  
![Login Success](public/results/login.png)

4. Go to profile with token  
GET http://localhost:3000/api/auth/profile  
Headers: Authorization: Bearer <token>  
![Profile With Token](public/results/profile_with_token.png)

