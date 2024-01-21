# Very basic auth server

Provides login and auth routes that encode and decode JWT's for a basic authentication service.
Note - users are hardcoded.

## Setup

```sh
cargo install
cargo run
```
Now you can curl requests to 127.0.0.1:8000

## Usage

### login 

returns a token

```sh
curl http://127.0.0.1:8000/login -d '{"email" : "johndoe-admin@mail.com", "password" : "test1"}' -H 'Content-Type: application/json'
```

### user

supply a token and check if you're authorized

```sh
curl http://127.0.0.1:8000/user -H 'Authorization: Bearer <token from first step>' -H 'Content-Type: application/json'
```