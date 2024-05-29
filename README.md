### This is the Backend Challenge from Instituto Atlântico.
##
### First of all you need:
  - Java 17
  - Docker
  - Postman(or anything else you wish to send requests)
  - IDE of your preference

Images you need to pull from Docker <  https://hub.docker.com/  >
    *ps: You need to be logged in Docker in order to be allowed to download the images od RabbitMQ and Postgres.
    **ps: Docker needs to be in Linux version.
    ***ps: The installation will take place when you run: "docker compose up --build" however it's not time to run it yet.

If you need password and some information about RabbitMQ, Postgres and API, visit a file named:
  <  application.yml  >

### RUNNING
##
  - At first, do get into the main directory where docker-compose file is located and run the following command:
            
            docker compose up --build

       ---What happened? The command you have just inserted into the terminal will build Postgres11, RabbitMQ13.3 and our API on Docker.

  - If you want to run it again and the project is already built, run:

            docker compose up

### REQUESTS
##
  - Check API status: http://localhost:8081/api/status

  - Check users: http://localhost:8081/api/all_users

  - Check subscriptions: http://localhost:8081/api/all_subscriptions

  - Check status: http://localhost:8081/api/all_status

  - Check evets: http://localhost:8081/api/all_events

  - Check user by id: http://localhost:8081/api/user/{User ID} 
    e.g. http://localhost:8081/api/user/1000

  - Check user by name: http://localhost:8081/api/subscription/name/{User Name} 
    e.g. http://localhost:8081/api/subscription/name/Matthews

  - Check subscription by id: http://localhost:8081/api/subscription/id/{Subscription ID} 
    e.g. http://localhost:8081/api/subscription/id/1000

  - Purchase a subscription: http://localhost:8081/api/subscription/purchase
            body: {
                      "name": "Paulo",
                      "status": "ACTIVATED",
                      "type": "PURCHASE"
                  }
  - Cancel a subscription: http://localhost:8081/api/subscription/cancel/{id} 
    e.g. http://localhost:8081/api/subscription/cancel/1000

  - Restart a subscription: http://localhost:8081/api/subscription/restart/{id} 
    e.g. http://localhost:8081/api/subscription/restart/1000
