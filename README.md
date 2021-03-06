# Knowledge-Based Engineering Project 

This project is a part of the course TMM4275 Knowledge-Based Enineering, Project. The main task is making an automatic KBE system for manufacturing a coustom chair. From taking the client's order, checking if the order is within the constraints set by a product engineer, then making a model of the chair and ordering it from the factory.
The customar should be able to specify different sizes and shapes for the different parts of the chair, making their own custom chair. 

This project is made by: 
* Kasper Kallseter
* Magnus Myklegard
* Amalie Berge Holm


### The Chair

The image below show a NX modelling of the cair: 
![Chair_NX](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Chair_NX.PNG)

the customer is able to define the following parameters for thir chair: 
* Length of legs
* Width of legs
* Height of the back
* Depth of the seat
* Width of the seat
* Length of apron


### The KBE Application Architecture

This is a diagram showing Client-Server architecture, and how the information travels through the different sercers and tools to make it possible for the customer to order the chair. 

![Client-Server](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Client-Server.png)


### An Order Making Scenario

This is an ULM sketch, showing how an order making scenario will play out. From the enineer defining constraits and the customer defining parameters for the chair, to the order being made. 

![ULM:PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/ULM.PNG)


### Development Tools

This code was made using python in Visual Studio Code. Knowledge Fusion was used in NX to make models of the chair and Olingvo and Apache Jena Fuseki was used to communicate with the server containing the parameters, set by both the customer and the product engineer. 

To run the code you will need to have a running Fuseki-Server and a correct Owl-file (in the Owl-folder) uploaded to the server. You also need to change the paths in the code, to match the paths on your own computer. 


### Code Description 

- `manufChecker.py` - Setting up the web-page which the product engineer uses to define the constraints, sending this to the fuseki server
- `DFAserver.py` - Setting up the web-page that the customer uses to place an order, checking it against the constraits given in the fuseki server, if the order is within the constraints, the order is made into a DFA file, visualized in NX

### OWLs
- `chair.owl` - File made in Olingvo, setting the properties(constraints) for the chair, and uploaded to Fuseki, making it reachable from the web-pages

### DFAs
- `My_Chair_template.dfa` - Containing the NX file of the chair template, this is used as the template which every oderer modify to the customers wishes
- `My_Chair_Order.dfa` - Containing the NX file whith the parameters given by the customer



## Examples of Three Different Product Orders  

### Product Engineer Setting Parameter Constraints
![Ex1%20-%20setParams.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex1%20-%20setParams.PNG)


### A Customer Trying to Order Outside the Constraints
![Ex2%20-%20orderChair.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex2%20-%20orderChair.PNG)



### Example 1 - Landscape Green 
![E1%20-%20orderChair.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/E1%20-%20orderChair.PNG)
![Ex1%20-%20chair%20NX.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex1%20-%20chair%20NX.PNG)



### Example 2 - Flaming Red 
![Ex3%20-%20orderChair.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex3%20-%20orderChair.PNG)
![Ex3%20-%20chair%20NX.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex3%20-%20chair%20NX.PNG)



### Example 3 - Icy Blue
![Ex4%20-%20orderChair.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex4%20-%20orderChair.PNG)
![Ex4%20-%20chair%20NX.PNG](https://github.com/amaliebholm/TMM4275-KBE-project/blob/main/Images/Ex4%20-%20chair%20NX.PNG)

