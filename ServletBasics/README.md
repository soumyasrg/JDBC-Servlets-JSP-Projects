<h2> Servlet Life Cycle Methods and Phase </h2>
<pre>
if you have run a java standalone program then you know that the starting point for every java program is the main
method which is the only method which in turn calls the other methods We write 
whereas for a servlet there are three lifecycle methods starting with the unit, service and destroy 
and there are four life cycle phases associated with these three methods
They are instantiation, initialization, servicing and destruction, these lifecycle methods are called
by the container so the web containers like Apache Tomcat will first go through the instantiation phase
where they will create a instance of our servlet class by loading it into memory.
So if we are working on an e-commerce application where we have a order servlet that takes the order
from the web browser from the client and then it saves that order into the database the container will First load 
this order servlet class into memory and then will create an instance of it.
That is called the instantiation phase.
It will then call the init method on servlet,this is where we should write code which will be run only once.
This init method is called only once by the container.
So if we want to create database connections this is a good place to put that code.
Then it calls the service method ,this service method is all our business logic goes this is where we
can write all the code that saves it out of the database or retrieve data from the database or any other
processing logic.
This Service method is called n times
That is if there are 100 clients using hundred browsers they are sending hundred requests.
This service method will be called a hundred times.
So if there are thousand orders placed by different clients thousand clients then this method will be called
thousand times finally the destroy as itself says it does the opposite of or we should put the
code which does the opposite of what the unit method does.
So putting the code into these methods is our responsibility but calling them is the containers responsibility.

So this destroy is also called only once, the servlet container calling the destroy method is nothing but
destruction and the container cost the service method it's called Servicing
So to summarize there are three life cycle methods for every servlet and for life cycle phases the servlet
container is responsible for instantiating the servlet initializing it by calling the unit method and then
servicing it.
And finally destruction destroying the servlet as well.
</pre>


<h2>Web Application Folder Structure</h2>
<pre>
oracle provides a standard folder structure that every java EE application should follow
in order for it to be deployed on a application server or web container like Tomcat.
The first folder is the root folder which is the web application name it could be Amazon, Twitter or your
own web application for which you are working on.

Below it will place our HTML pages and jsp s directly or we can create sub folders and create them there.

So when a request comes in for a html or a jsp, resource containers like Tomcat will directly search
under the backup or under the subfolders on it. 
Depending on the url the next important folder is WEB-INF
This is a standard from oracle
So we need to follow this when we deploy it to Tom-Kat or any other application server
web-inf will have web.xml 
we create this file; this is a deployment descriptor file or a configuration file
which we as developers use to configure our servlets filters, welcome Pages and many more for our 
web application.
This acts as a interface between we as developers and the web container like Tom-Kat
classes has the name itself says is where all our class files.

Servlets listeners or dao classes data access layer classes were we put all of our database
code or business logic classes where we put all our business logic all the classes will go under the classes
folder.
finally the lib directory libraries will go here jars 
so Tom-Kat and another containers will search for classes both under classes folder as well as inside the jars.
Under the lib folder typically in real time applications we make a jar file of all the classes in the
application and put it under the Lip folder we rarely use the classes folder
It is used locally for testing any third party libraries like Hibernate or my sql jar or even
Oracle jar oracle driver jar
All those will go on to the lib folder ids like Eclipse might not follow the exact folder structure.
When you create a web application in Eclipse but when you run the web application and when eclipse deployes
it to Tom-Kat it will follow this standard Behind the scenes.
So don't get confused when ever we deploy web applications onto any container.

This is the folder structure you will have to follow and you will see but 
u rarely have to create this folders manually.
Ides like  Eclipse will do it for you.

The second way easy way to do it is a war file
You will learn more about a war file and how to deploy using a War file in lectures later on.
Eclipse can create a war file out of the web applications you create very easily and we can take that War file and
deploy it to tomcat or any other application server.

</pre>

<h2> </h2>


