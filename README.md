# findDivisible
This program finds the numbers divided by the number you want in the range of values ​​you enter with 1.


version: "3.8"

services:
  web:
    image: nginx:latest
    ports:
      - "80:80"
    depends_on:
      - app

  app:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db

  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: testdb
