Scala example with playframework and slick
==========================================
[![Build Status](https://travis-ci.org/fancywriter/car-adverts.svg?branch=master)](https://travis-ci.org/fancywriter/car-adverts)
[![Code Coverage](https://codecov.io/github/fancywriter/car-adverts/coverage.svg?branch=master)](https://codecov.io/github/fancywriter/car-adverts?branch=master)

# Car Adverts RESTful service
To run application just type `sbt run`

Application supports the following methods:
 - **GET /adverts** - list all adverts
 - **GET /adverts/{id}** - find by id
 - **DELETE /adverts/{id}** - delete by id
 - **PUT /adverts/{id}** - update (modify) existing advert
 - **POST /adverts** - create new advert

All adverts have the following fields:
 - **id** (UUID, required)
 - **title** (string, required)
 - **fuel** (string/enum, required)
 - **price** (integer, required)
 - **new** (boolean, required)
 - **mileage** (integer, optional) - only for used cars (new = false)
 - **firstRegistration** (local date, optional) - only for used cars (new = false)

Application uses H2 embedded database in-memory. No need to prepare anything.
