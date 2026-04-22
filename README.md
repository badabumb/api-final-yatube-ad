# API for Yatube

REST API for the Yatube training project. The service exposes publications,
comments, groups, subscriptions, and JWT authentication endpoints documented in
Redoc at `/redoc/`.

## Local setup

1. Create and activate a virtual environment.
2. Install dependencies:
   `pip install django djangorestframework djoser djangorestframework-simplejwt pytest pytest-django`
3. Apply migrations from the project directory:
   `python manage.py migrate`
4. Start the server:
   `python manage.py runserver`

Project root for Django commands: `/Users/juliavediukova/STUDY/Dev/api-final-yatube-ad/yatube_api`

## API examples

Get all posts:
`GET /api/v1/posts/`

Create a post with JWT:
`POST /api/v1/posts/`

```json
{
  "text": "My first post",
  "group": 1
}
```

Get comments for a post:
`GET /api/v1/posts/1/comments/`

Create a follow:
`POST /api/v1/follow/`

```json
{
  "following": "author_username"
}
```

Get JWT tokens:
`POST /api/v1/jwt/create/`

```json
{
  "username": "TestUser",
  "password": "1234567"
}
```
