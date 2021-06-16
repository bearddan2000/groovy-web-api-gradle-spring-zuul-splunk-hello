# groovy-web-api-gradle-spring-zuul-splunk-hello

## Description
A springboot app that uses zuul
as a reverse proxy. All requests
to `/api` will be forwarded to nodejs
server. Uses splunk to centralize logs.

### STEP 1
Once the project is done building, make
some api calls `http://localhost:81/all`.

To see logs in Splunk:
- Nav to http://localhost
- Login with `admin/password`
- Search with log id
  - Log id can be found on console after api calls

## Tech stack
- groovy
- gradle
  - springboot
  - netflix zuul
- nodejs

## Docker stack
- gradle:jdk11
- node:latest
- splunk/splunk:8.0
- splunk/universalforwarder:8.0

## To run
`sudo ./install.sh -u`
- SPLUNK DASHBOARD http://localhost
  - Login with `admin/password`
- API http://localhost:81/all
- REMOTE API http://localhost:81/api/all

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credits
- https://spring.io/guides/gs/routing-and-filtering/
