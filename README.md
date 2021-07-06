# Bank_Note_Auth_flasgger_Docker




## DOCKER:

Docker is a set of Platform As a Service(PAAS) products that uses OS-level virtualization to deliver software in packages called containers. 
Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels
Advantage of Docker is that, it does the Environment Standardization, Isolation, Portability and we need to build ONCE and Deploy it anywhere.
Virtual Machine also works like Docker, but in that case resource allocated to 1 VM cant be shared by other VM, If 1 VM is not working. So no portability in VM .
In Docker we have process id,N/W config, Root folder etc


## FLASGGER library:

This is to develop front end BY using Flask.
Flasgger is a Flask extension to extract OpenAPI-Specification from all Flask views registered in your API. 
Flasgger also comes with SwaggerUI embedded so you can access http://localhost:5000/apidocs and visualize and interact with your API resources.

Before while using flask we created template folder for frontend html web page generation, but with flasgger no need that, just using SwaggerUI will do basic front end web page development (Flask+Swagger =Flasgger) 

### SWAGGER: 

Swagger is api thing, it will automatically generates front end . We need to follow some steps inside app.py file.

Install flasgger 
pip install flasgger
