
## Deployment instructions

1. Build the Docker image:
```
$ docker-compose build
```
1. Boot the app:
```
$ docker-compose up
```
1. Create the database. In another terminal, run:
```
$ docker-compose run web rake db:create
```
1. View the welcome page:
http://localhost:3000
1. Stop the application:
```
$ docker-compose down
```
1. Restart the application:
```
$ docker-compose up
```
1. Rebuild the application:
  - If you make changes to the Gemfile or the Compose file:
  ```
  $ docker-compose up --build
  ```
  -  full rebuild requires a re-run of
  ```
  $ docker-compose run web bundle install
  ```
  to sync changes in the `Gemfile.lock` to the host, followed by `docker-compose up --build`.

## How to run the test suite
