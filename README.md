# WcfServiceApplication
#this project is a basic WCF Service application:
I have described how to create it in VS2019 and how to test it by “WCF TEST CLIENT.exe"

how to create WCF service  project in VS2019?
This is an article  how to create a very basic WCF application for the first time; here I have explained the step by step process to create a WCF application using Visual Studio 2019
What is WCF Service
Windows Communication Foundation (WCF) is a framework for building service-oriented applications. Using WCF, you can send data as asynchronous messages from one service endpoint to another. A service endpoint can be part of a continuously available service hosted by IIS, or it can be a service hosted in an application.
Application Creation and Hosting
I have provided a step by step procedure to create the WCF application using VS2019 and also WCF service can be hosted and tested in multiples and here I have shown testing the application using the “WCF Test Client” which is built  in and available when you install the Visual studio.
WCF Application Creation Procedure
Step 1

Open the Visual Studio and create a “New Project”in the Search field write wcf  and select WCF Service Application as following image:


Press Next then give a project name (WcfServiceApplication), select location, framwork as shown in bellow:

Press Create then project is created and shown as bellow:

Step 2
On Successful project creation, now Visual studio gives us the option for automatic code sample.
What is automatic code Template in the Visual Studio?
Yes, whenever you create a WCF application using visual studio, it will create the default template as it creates for other applications and this will gives you a very good sample application, let’s see in detail.
The following files are created and also the required assembly files are also added to the solution automatically,

All the references are added and some of the references are highlighted with red points for your visual.
Files Available in the solutions

Following files are created:
IService:  Service Interface File
Service.SVC:  It’s the file where Service code is available and similar to .asmx file of web service
Web config: Configuration details where the Endpoint information are stored.
IService.cs
This is the file which has all the declarations rahther than definition of properties, here we call it Contract in WCF and this helps for all the operations that happen with the service named “Operation Contract”.
Operation Contract: The method is declared and where the actual implementation is done in .SVC file, each contact has to be decorated with the appropriate Attribute tags
and here is Service Contract as shown below.

Data Contract
Here the Data are to be transferred and processed within service and they store the values, so in the WCF terminology they are called “Data Contract”.
Where each member of the Class; i.e., the Data contract is called “Data Member” and they are also to be decorated with the Attributes.

Service.SVC
This is the main file for any of the WCF services where this file inherits the “IService” interface and implements all the methods of the operation contract methods.
Web config:
In a WCF application Web config files play another important role, as the application will have various set of “ABC”- Address, Binding and Contract and all those are defined in the web config files.
Sample Config Entries
paste here
Execute the Application using WCF Test Client
The WCF Test Client is one of the best tools for developers to test the WCF application.
Windows Communication Foundation (WCF) Test Client (WcfTestClient.exe) is a GUI tool that enables users to input test parameters, submit that input to the service, and view the response that the service sends back. It provides a seamless service testing experience when combined with WCF Service Host.
This file will be available in the following location,
C:\Program Files (x86)\Microsoft Visual Studio (Your Version Here)\Common7\IDE
if you start it shall be as bellow:

Step 3
Set the Service.SVC file as the “Start up page”
displayed.

execute the application by pressing to the  IIS Express button on VS2019
 so automatically the WCF Test client window will be displayed. as bellow:

We see that two methods are supported (GetData() and GetDataUsingDataContract()) 
and the red crossed methods are not supported.
Step 4 – WCF Test Client Execution

Here all the Methods will be displayed and also the appropriate method details will be displayed on the right side pane when you select the methods, which are readily testable.
Step 5
Double click  on “GetData() method in the left side an write a value (4567) in the right side and press to the Invoke button as shown in the bellow:

“Invoke” method will execute the method with the input value and gives us the response from the service and you can view the response in the application output section of WCF test client.
Step 6
by pressing Invoke the method GetData() is invoked and sent to Service and got response as bellow:

The response value is “you have got the response value 4567.
Conclussion:
We have created the WCF  Service application and also tested using a “WCF TEST CLIENT”
We have done a sample without writing a single line of code and that was the ease of usability of the Visual studio.
In my Next post shall describe and implement ??
Read More >> A Complete WCF Tutorial Series from Beginner to Advanced
