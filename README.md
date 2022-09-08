# ABET-APP

'Description of the full web application'

## How to install and run

1. Clone this repository running the comand `git clone https://github.com/Yotas01/ABET-APP`
2. We advise opening the project with [VSCode](https://code.visualstudio.com) to build the **Front-end** and the **Back-end**. To do this go to the ABET-Back-End folder and run the following command:
    `./gradlew build -x test`
  
This will build the Back-End and package it in a .jar. Now to build the Front-End go back to the Front-End folder and run:
    ```
    npm install
    ng build
    ```
Once both projects have been built, you can now run the Docker compose file. To do this return to the root folder of the ABET-APP project and run:
    `docker-compose up --build`
  
This will create the Docker container with the images for the MySQL Database, the Spring Boot Back-End and the Angular Front-End. If you want to create the QA environment for the application, run the same docker command from the 'qa-env' folder.