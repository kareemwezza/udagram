## App dependencies

**For BackEnd**

- Node Js
- Sequelize
- Express JS
- JsonWebToken

**For Frontend**

- Angular
- Ionic
- Zone.js

## App Infrastructure

Application is build on 3 compartment:

- Frontend compartment deployed on aws S3 services that all clients can interact with.
- Backend compartment deployed on aws EB service that receive all api requests from frontend and sends responses back
- RDS are connected to to the backend that hold all the data of the clients and sent to the application.

![Alt text](./infrastructure.png?raw=true "App Infrastructure")

## App pipeline process

- Upon every change on main branch on Udagram repository process of CI starts.
- Node Environment is setup on docker image with version compatible with local node version.
- Front end dependencies are installed.
- Backend API dependencies are installed.
- Linting Front End API.
- Start build process for Front End.
- Start build process for Backend.
- Beyond application build the process is hold for manual approval.
- After manual approval deployment process on AWS web services start.
- Front end is deployed on Amazon S3 web services.
- Backend is deployed on Amazon Elastic beanstalk.

![Alt text](./pipeline-process.png?raw=true "Pipeline process")
