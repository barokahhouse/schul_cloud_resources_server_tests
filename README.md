# Schul-Cloud Ressources Server Tests

This repository contains

- a server to test scrapers against
- tests to test the server

## Installation

Using `pip`, you can install all dependencies like this:

    pip install --user -r requirements.txt test-requrements.txt

## Server

You can find the API definition [here][api].
The server serves according to the API.
It verifies the input and output for correctness.

To start the server, run

    python3 -m schul_cloud_ressources_server_tests.app

## Tests

You always test against the running server.
**Tests may delete everyting you can reach.**
If you test the running server, make sure to authenticate in a way that does not destroy the data you want to keep.

    pytest --pyargs schul_cloud_ressources_server_tests.test --url=http://localhost:8080/v1/



[api]: https://github.com/schul-cloud/ressources-api-v1
