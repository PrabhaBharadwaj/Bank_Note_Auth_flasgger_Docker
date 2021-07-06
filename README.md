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


### 1) app.py
	
	--> Inside this some commented part are very important related to swagger. so we need to follow properly as same.
	-->All indentation we should follow properly, else swagger page wont opens properly

		    """Let's Authenticate the Banks Note 
		    This is using docstrings for specifications.
		    ---
		    parameters:
		      - name: file
		        in: formData
 		       	type: file
 		       	required: true
      
		    responses:
		        200:
   		         description: The output values
 		       
  		  """

	here 'in' is fromdata, query(Input value) etc
		'name' is 'Columnname'
		'type' is which type like number,float, string,file etc
		'required' is weather column value is compulsary or not

### 2) Run this app.py in spider or cmd project specific env

	--> We get link http://127.0.0.1:5000/  once we run there, we get below message
				Welcome All

	--> just copy that link and append /apidocs/ and paste in Chrome
			http://127.0.0.1:5000/apidocs/
		We will get the Swagger API page with all our function written in app.py
		
	--> We get 2 tab:
	#####	1) GET ​/predict Let's Authenticate the Banks Note
			Press-> Try it out
			If we press that we get input window to pass 4 variable values  --> Execute
			We get message in "Response body" as "Hello The answer is[0]"


	#####	2) POST ​/predict_file Let's Authenticate the Banks Note
			Press-> Try it out
			If we press that we get input window to upload file-->Upload local file TestFile.csv  --> Execute
			We get message in "Response body" as "[0, 0, 0, 0, 1, 1, 1, 1, 1]"

### Docker container:
		Above we built Flasgger used api.py. Now we are building docker container to deploy this in different environment in few steps
