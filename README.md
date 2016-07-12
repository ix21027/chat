# Rails Chats API - Sample Application

## Install

### Clone repository
```
git clone https://github.com/MLSDev/rails-chats-api
```

### Install gems
```
cd rails-chats-api
```

```
bundle install
```

### Run migrations
```
rake db:migrate
```

### Run specs
```
rake
```

### Run server
```
rails s
```

## API documentation

### Sign Up
```
curl -d 'user[email]john@mcclane.com&user[password]=superhero&user[password_confirmation]=superhero' localhost:3000/profile
```

### Sign In
```
curl -d 'session[email]=john@mcclane.com&session[password]=superhero' localhost:3000/session
```

### Get own Profile info
```
curl -H 'Authorization: Token token="XXXX-YYYY-ZZZZ"' localhost:3000/profile
```

## TODO

### Sign Out

```
curl -H 'Authorization: Token token="XXXX-YYYY-ZZZZ"' -X DELETE localhost:3000/session
```

### Customize Profile Info

Request
```
curl -H 'Authorization: Token token="XXXX-YYYY-ZZZZ"' localhost:3000/profile
```

Response
```json
{ "email": "john@mcclane.com" }
```
