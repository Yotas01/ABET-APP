# ABET-APP

'Description of the full web application'

## How to install and run locally

1. Clone this repository running the comand `git clone --recursive https://github.com/Yotas01/ABET-APP`
2. We advise opening the project with [VSCode](https://code.visualstudio.com) to build the **Front-end** and the **Back-end**. To do this go to the ABET-Back-End folder and run the following command:
    ```
    ./gradlew build -x test
    ```
    This will build the Back-End and package it in a .jar. Now to build the Front-End go back to the Front-End folder and run:
    ```
    npm install
    ```
    and then
    ```
    ng build --configuration=local
    ```
Once both projects have been built, you can now run the Docker compose file. To do this return to the root folder of the ABET-APP project and run:
    `docker-compose up --build`
  
This will create the Docker container with the images for the MySQL Database, the Spring Boot Back-End and the Angular Front-End. If you want to create the QA environment for the application, run the same docker command from the 'qa-env' folder.

If you want to run the Angular APP live and not in the Docker container, stop the ABET-Front-nd Docker image and go to the Front-End folder and run the command:
 `ng serve --configuration=local`

## How to install and run remotely
If you are deploying the application in the server follow the next steps instead:
1. Clone this repository running the comand `git clone --recursive https://github.com/Yotas01/ABET-APP`
2. Open the new ABET-APP folder and inside there should be 2 more folders: 'ABET-Back-End' and 'Front-End' Go to the 'ABET-Back-End' folder and run the command
    ```
    gradle build -x test
    ```
3. Go to the Front-End folder and run the command
    ```
    npm install
    ```
    and then
    ```
    ng build
    ```
    To build the Front-End.
4. Go back to the ABET-APP folder and make sure there are no running containers by running the command `docker-compose ps` and if there are any containers running, stop them with `docker-compose stop`. Once you know there are no containers running run the commmand `docker-compose up --build -d` to start the container with the app      running
