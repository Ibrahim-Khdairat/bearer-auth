# LAB - 07 bearer-auth


**Author: Ibrahim Khdairat**

### Deployment Test


- [back-end](https://ibrahim-bearer-auth.herokuapp.com/).
- [pull request](https://github.com/Ibrahim-Khdairat/bearer-auth/pull/1).

**Setup**

`.env` **requirements**

- `PORT` - Port Number

- `DATABASE_URL` = Postgres DB

- `SECRET` = JWT SECRET

**Running the app**

- `npm start`

- Endpoint: `/signup`

> `{"username": "ibrahim-kh","password": "pass123"}`

- Returns Object

     {
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0ta2giLCJpYXQiOjE2Mjk3NTEzMjZ9.L18GhBdEm1rSxThPYoQQH4SBKXSAQ_01UJlId74UHQY",
        "id": 2,
        "username": "ibrahim-kh",
        "password": "$2b$10$ghMj3qEwUVyygZ8JZaBAt.RN.p/D37mSiurlOdGkELZyr07wZT73.",
        "updatedAt": "2021-08-23T20:42:05.344Z",
        "createdAt": "2021-08-23T20:42:05.344Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0ta2giLCJpYXQiOjE2Mjk3NTEzMjZ9.L18GhBdEm1rSxThPYoQQH4SBKXSAQ_01UJlId74UHQY"
}

- Endpoint: `/signin`

> - Username `ibrahim`
> - Password `pass123`

- Returns Object

     {
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0iLCJpYXQiOjE2Mjk3NTExNjN9.8B0y3uymEVkpBM4TAToeTNtFm83WSz6k-SAT3pUG3BA",
        "id": 1,
        "username": "ibrahim",
        "password": "$2b$10$LuTCPKkr8Qc0l/vryNWzMexa5QjuTE66fzCwsoBecYkFaImTP/6qi",
        "createdAt": "2021-08-23T20:37:48.221Z",
        "updatedAt": "2021-08-23T20:37:48.221Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0iLCJpYXQiOjE2Mjk3NTExNjN9.8B0y3uymEVkpBM4TAToeTNtFm83WSz6k-SAT3pUG3BA"
}

- Endpoint: `/users`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0iLCJpYXQiOjE2Mjk3NTExNjN9.8B0y3uymEVkpBM4TAToeTNtFm83WSz6k-SAT3pUG3BA`

- Returns Object

  [
  "tariq"
  ]

- Endpoint: `/secret`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImlicmFoaW0iLCJpYXQiOjE2Mjk3NTExNjN9.8B0y3uymEVkpBM4TAToeTNtFm83WSz6k-SAT3pUG3BA`

- Returns Object


**Tests**

- Unit Tests: `npm run test`
- Lint Tests: `npm run lint`