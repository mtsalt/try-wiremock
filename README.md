# try-wiremock
This repository is for trying out wiremock. It can be easily executed in an environment where docker compose is installed.


# Hot to use

1. Set ```__files``` and ```mappings``` at ```wiremock_data``` directory
1. Start environment  
    ```
    docker compose up -d
    ```
    **When change the wiremock port, check .env file (default 8080)**
1. Request
    - GET
        ```
        curl http://localhost:8080/try-wiremock -H 'Content-Type: application/json'
        ```
    - POST
        ```
        curl http://localhost:8080/try-wiremock -H 'Content-Type: application/json' -d '{"data" : "hello from client"}'
        ```
1. Rload mappings
    ```
    http://localhost:8080/__admin/mappings/reset
    ```