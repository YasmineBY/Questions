# Questions
All questions for Mobile Development


# Lesson 1

#What are the names of the latest three versions of Android?  

Android Nougat,
Android Oreo,
Android Pie

#What does the abbreviation ART stands for?

Android Runtime

#What is Android Jetpack?
 
Jetpack is a suite of libraries, tools, and guidance to help developers write high-quality apps easier. These components help you follow best practices, free you from writing boilerplate code, and simplify complex tasks, so you can focus on the code you care about.
 
#Describe the difference between the fixed, wrap_content and match_constraint setting of the constraint layout?


Wrap content makes sure the item isnt bigger than the space it needs (Like a box in a recyclerview, its length isnt suppose to take up the entire screen). 

match_constraint will take up all the space that it can.
 
#What does the abbreviation DP stand for and why do we need them? 

density-independent pixels (dp) as your unit of measurement. One dp is a virtual pixel unit that's roughly equal to one pixel on a medium-density screen (160dpi; the "baseline" density). Android translates this value to the appropriate number of real pixels for each other density.
 
#What is the purpose of the string.xml file? 
 
To store Strings. This way you don't get any 'hardcoded' strings and you can easily change text instead of having to click on each item from your layout seperatly. (This goes especially for when you reuse a string multiple times)
 
#Why is the layout in Android specified by .xml files?  Why not just have the layout in the code (Kotlin or Java)? 


Declaring your UI in XML allows you to separate the presentation of your app from the code that controls its behavior. Using XML files also makes it easy to provide different layouts for different screen sizes and orientations.
 
#What kind of information can be found in the manifest file? 


The manifest presents essential information about the application to the Android system, information the system must have before it can run any of the application's code. Among other things, the manifest does the following:

It names the Java package for the application. The package name serves as a unique identifier for the application.
It describes the components of the application — the activities, services, broadcast receivers, and content providers that the application is composed of. It names the classes that implement each of the components and publishes their capabilities (for example, which Intent messages they can handle). These declarations let the Android system know what the components are and under what conditions they can be launched.
It determines which processes will host application components.
It declares which permissions the application must have in order to access protected parts of the API and interact with other applications.
It also declares the permissions that others are required to have in order to interact with the application's components.
It lists the Instrumentation classes that provide profiling and other information as the application is running. These declarations are present in the manifest only while the application is being developed and tested; they're removed before the application is published.
It declares the minimum level of the Android API that the application requires.
It lists the libraries that the application must be linked against.

-----------------------------------------------------------------------------------------------------------
# Lesson 2

#What is the difference of a staggered grid comparing to a normal grid?

Grid View : It is is a ViewGroup that displays items in a two-dimensional, scrollable grid. In this each Grid is of same size (Height and width). Grid View shows symmetric items in view.

Staggered Grid View : It is basically an extension to Grid View but in this each Grid is of varying size(Height and width). Staggered Grid View shows asymmetric items in view.

#What is the purpose of logcat?  

Logcat is a command-line tool that dumps a log of system messages, including stack traces when the device throws an error and messages that you have written from your app with the Log class.

#What kind of gestures are available?

Ontouch and motion.


#What was the predecessor of the recyclerview?

Listview


#What is the difference between a Toast and Snackbar ?

Toast:

    Toast was added in API Level 1
    Basically Activity is not required (Can be shown on Android home or even above other apps)
    It can’t perform an action based on User input
    It can’t be dismissed by swiping
    It can’t handle user input like Swipe, Click etc.
    Good for showing info messages to user

SnackBar:

    SnackBar was added in API Level 23
    It can be showed inside an activity of the Applications
    It can perform an action
    It can be dismissed by swiping
    It can handle user input
    Good for showing warning/info type messages to user that needs attention


#What is the purpose of the existence of “optionals” in the Kotlin language?

To prevent Nullpointer exceptions

-----------------------------------------------------------------------------------------------------------
# Lesson 3

#Which stages of an activity lifecycle exists?
   - Oncreate(), Onstart(), OnResume(), OnPause(), Onstop(), OnDestroy(), OnRestart()

#Which are the two kind of intents, and what is the difference?

Explicit intents, Implicit intents
Implicit intents Specifieert alleen de class en geen actie. (Zoals een app chooser)

#What is the difference between Parcelables and Serializables?

Serializable is a standard Java interface. You can just implement Serializable interface and add override methods. The problem with this approach is that reflection is used and it is a slow process. This method creates a lot of temporary objects and causes quite a bit of garbage collection. However, Serializable interface is easier to implement.

Parcelable process is much faster than Serializable. One of the reasons for this is that we are being explicit about the serialization process instead of using reflection to infer it. It also stands to reason that the code has been heavily optimized for this purpose.

#What is the purpose of the analyzer?

Analyseert je code op xml, kotlin en android standarden zoals: hardcoded text, redundant semicolons etc.

-----------------------------------------------------------------------------------------------------------
# Lesson 4

#A singleton pattern is used in the class that defines the database. What is the purpose of this pattern?

To ensure there are no two instances of the database

#Why should you load the data in a background thread?

Because that costs alot less capacity

#What are the three major components of ROOM and what are their responsibilities?

Database: It represents the DB, it is an object that holds a connection to the SQLite DB and all the operations are executed through it. It is annotated with @Database.
 
Entity: Represents a table within the Room Database. It should be annotated with @Entity.
 
DAO: An interface that contains the methods to access the Database. It is annotated with @Dao.

#How can you extract the current database so that you can see the table, columns, and data?

I'm not sure what this question is saying, but you can use queries to retrieve the data.
