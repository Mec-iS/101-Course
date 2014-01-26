#Welcome!
----
We are here to let you folks get in touch with Google App Engine (since now GAE), a developer-friendly environment to design and realize apps powered by Google hosting/computing services, Big Table database, and other Google goodies.
<br/>
The GAE's presentation as Google Cloud service [here](https://developers.google.com/appengine/). All the docs are accessible from the left-side menu.
<br/>

As you can see, you can develop with GAE by two stable developing environment: Java and Python. And two experimental one: PHP, Go. This doc will focus on Python developing, as the author thinks it's the most enjoyable of the four.

To know a little more about Python you can read this really great articles:

* [Why Python Is More Fun Than Java](http://brizzled.clapper.org/blog/2008/07/28/why-is-python-more-fun-than-java/)

* [Why Python Is The Best](http://www.linuxjournal.com/content/why-python-best)

I just find Python to be more productive and fit for solo developing, easy to find docs and examples, and really tuned to OpenSource community. A lot of free books can be found on the Internet, to learn to be a better Python programmer. It is also proved that Python is the most [newbie-friendly programming language](http://stackoverflow.com/questions/3088/best-ways-to-teach-a-beginner-to-program)... probably (:

This course is based on the experience made with:

* [Udacity CS253 course](https://www.udacity.com/course/cs253)
* [Programming Google App Engine second edition](http://shop.oreilly.com/product/9780596522735.do)

Thanks!
---
<br/>

## **Google App Engine** is a [Platform as a Service](http://en.wikipedia.org/wiki/Platform_as_a_service).

Google provides all the tools you need, from the hardware to the top-stack, to host and develop your apps, all wrapped into a service that take a shape of a platform (or something you can use to found your work over).

GAE is free for any basic/learning usage you would like. The pricing is **0$ under defined quotas**, over these level of usage you are going to pay the resource based on time or number of request. Free of charge quotas are quite enough for low-traffic site, and more than enough for learning purpose. You can also just decide to avoid your app serving when it receives requests exceeding the free quotas. Check the [quotas](https://developers.google.com/appengine/docs/quotas) and [pricing](https://developers.google.com/appengine/pricing) before starting to be sure about what you get. 

As far as I know GAE is a good service, and helped me to start my own activity without getting mad about sys-administration.

GAE runs by mean of:

* A *runtime environment* (or more rudely a 'sandbox'). A kind of place on top of the hardware+software stack where the things you program run and do the job they have been programmed for. With GAE you have the same environment running remotely on the Google cloud but you, also, can run your local environment on your computer for testing/developing purpose. Any time you would like to make your app public and accessible from the Internet you will need to deploy it through the App Engine tools, from your computer to the cloud by the [App Engine SDK](https://developers.google.com/appengine/downloads)  

* By the Runtime Environment you can develop for, access and use many kinds of different services useful for your apps, the main [GAE's available features](https://developers.google.com/appengine/features/#generally_available_ga_features) are:
	* the Static File Server - to serve your javascript, css or images (one of the main security rule of GAE is that you cannot write on the filesystem of the machine running the app, but GAE provide a lot of nice feature to make you avoid doing this, like datastore and cache memory)
	* the Datastore - GAE lets you use the power and scalability of Big Tables, the database where Google services lay on. It's my favourite part of the platform, and its accessibility and speed is wonderful. It can be used as a full features Object Oriented datastore.
	* Services - GAE is fully integrated with any of the services accessible by Google APIs, with the rules defined for GAE. The list of Google available APIs can be found in your Google [APIs control panel](http://code.google.com/apis/console). 

You can access also your [App Engine Console](https://appengine.google.com/) inside cloud services website *to control how your apps are working*, or to create a new app. One of the nice parts is that you dont need to set up your own server like Amazon AWS or any other VPS or Computing provider, you just need to get in touch with 

---
<br/>

## Going to develop with GAE
1. To run a GAE development server you need to have **Python** (or any of the other supported programming languages) installed. GAE by now works perfectly with any [version 2.7+ of Python](http://www.python.org/getit/). Set up your Python, there are a lot of docs and tutorials around.

2. Download and Install the [GAE development kit](https://developers.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python) in a directory fitting your preference, if you want the SDK commands to be accessible from your projects' directory you should add it to the list of your environment's variables.

3. Login with your google account and go to [App Engine Console](https://appengine.google.com/). Create your app finding an available name. The app's domain will be choose-your-name.appspot.com That's the address where your app will be published. 

4. You can find a *new_project_template* dir, in you SDK directory. You can copy and paste it anywhere to have a starting framework for your GAE project. Those files are the real basic files for a GAE app:

	* *app.yaml* is where the basic settings for the app are stored, the GAE's runtime environment looks for this file any time is run. 

	* *index.yaml* is where datastore indexes are defined, you can forget about it by now, cause GAE will write it for you. You will need to edit it only when the app will be asked to perform quite complex datastore operations.

	* *main.py* is where the big part of the job is made. All you app's code will be written into or loaded by this file. 

---    
<br/>

## Start Learning Programming

### Vocabulary

An **algorithm** is a *procedure* in which some inputs get elaborated and outputs served.
An algorithm can be both hardware and software. 

Example: A router is an application of an algorithm, the electrical schema that funds the router's hardware is an algorithm; a browser is an algorithm itself as well, it's a set of instructions that perform a task. Software products are the most common family of algorithms around. 

Both perform actions in a stepwise way to achieve a result, they tend to be efficient and effective, and consistent.
In the Web protocols are software that runs on standard hardware, servers, they are both a different shapes of the concept of algorithm.
Algorithm tells and perform procedures for interpretation, translation, execution of any tasks on the Web.

**Programming languages** are languages to translate *procedures* to solve problems *into code* the computer can process.

Most of the modern programming languages use *Objects*, and are called *Object Oriented* (OO), to distinguish their approach from procedural (strictly stepwise, usually older) languages. Most of the OO languages can be used in a procedural (stepwise) way.

<u>Any programming language, or language's library or framework or protocol, is defined, or is the implementation of,  an [API](http://en.wikipedia.org/wiki/Application_programming_interface) (**Application Programming Interface**)</u>: 
 that is a collection of *functions, methods, Objects, procedures* or whatever makes any task working in that language, library or framework or protocol.

We are going to learn what is an API, a reserved key and the use of *this* keyword *through http://codecombat.com/*, a Javascript programming learning platform by gaming. Javascript is the OO programming language that works in any Web browser, in pair with HTML.

Any task implies to manage some input and outputs. They contains data, data is described by **data structures**, that are the basic standards for any data manipulation, exchange, encryption or any other possible use.

### Basic Concepts
Basic data structures are: **variables, sets, lists, dictionaries**.

```
# Variables
a = 5  
# variable assignment: *a* is now associated (referenced, pointed) to the number 5

# Sets
a = (1, 3, 5, 7)
# thisis a set of integers

# Lists (in Python, they can be also be found as vectors, arrays)
a = [1, 2, 3, 'name', 'things', variable] 
# lists are ordered sets of any kind of thing you can into a program

# Dictionaries (in Python, they can be found also as collections)
a = {'one': 'dog', 2: 'sun', 'three': 3, 5: ['one', 'two', 3] } 
# they are mapping structures, they associate a key (immutable) to a value (mutable)

# All these different kinds of data formatting/ordering/mapping have been assigned to the variable *a* in these examples
# The calculator now knows how to find them just telling it *a*

print a
# By this command we tells to print on screen the current value of *a*
```
Other kinds of data structure are **queues, stacks and trees**.

### Data Types
Any data you collect and put into a computer has a **type**, any type of data is a family that defines built-in rules and methods to process that kind of data.

There are many different kind of programming languages, they use and handle data in different ways, they can have strong-typing or weak-typing, depending on how they treat different kinds of data that happened to be in the same instruction.

Common data types are:
```
SIMPLE_TYPES = (int, long, float, boolean, string, double)
# here the variable SIMPLE_TYPES is a set of variables that represent the different types data you can find in any programming language
```

### An Example Of Common Data Structure For The Web

A very popular data structure used in server-client communications is [JSON](http://en.wikipedia.org/wiki/JSON): "an open standard format that uses human-readable text to transmit data objects consisting of attribute-value pairs." 

We introduce here this kind of data formatting for web-transmissions by presenting a JSON implementation for geolocating and draw over maps: [GEOjson](http://geojson.org/). Here an example of JSON used for this purpose:
```
{ "type": "FeatureCollection",
    "features": [
      { "type": "Feature",
        "geometry": {"type": "Point", "coordinates": [102.0, 0.5]},
        "properties": {"prop0": "value0"}
        },
         { "type": "Feature",
        "geometry": {"type": "Point", "coordinates": [102.0, 0.5]},
        "properties": {"prop0": "value0"}
        },
         { "type": "Feature",
        "geometry": {"type": "Point", "coordinates": [102.0, 0.5]},
        "properties": {"prop0": "value0"}
        },
      ]
}
```
---
<br/>

## What's the workflow about

App engine is made of two main developer features: the local development web server and the remote public instance of the app.
These are your working environments, the first one is for programming/testing only purpose, the second is the official/production 
app folk is going to enjoy. 
This is a common pattern to work with App Engine:


* develop locally with SDK: a real appengineer should avoid using the laucher (; the command line is much more reliable and let you follow
any operation's flow directly on the console.
** find your local instance at http://localhost:8080 and test
** find your admin console at http://localhost:8000
* deploy your code to Google Cloud
* manage and control your app through [appengine admin panel](https://appengine.google.com)



After having installed Python and the SDK:
* use the [appengine admin panel](https://appengine.google.com) to register your app
* copy the new_project_template directory from the SDK directory to a place you want to develop your new app (ex. **/develop/myapp/**)

Inside this directory you will find your `app.yaml`, set the name of your app.
Everything about the app.yaml file can be found [here](https://developers.google.com/appengine/docs/python/config/appconfig)

From your app directory, you can run (you need the python path, Python installer should have done it for you, and the app engine path in your system environment variables.
For any need you could have, refer to [documentation](https://developers.google.com/appengine/docs/python/) ):
* [dev_appserver.py](https://developers.google.com/appengine/docs/python/tools/devserver): it's the local instance of the app, where you are goin to work most of the time doing your adjustments
* [appcfg.py](https://developers.google.com/appengine/docs/python/tools/uploadinganapp): you will use for configuring/uploading/downloading 
 your app and source code
* [bulkloader](https://developers.google.com/appengine/docs/python/tools/uploadingdata): usefull to upload/download datastore data to/from the remote instance


For example (from the **/develop/** directory):
* the command:
```
python appcfg.py update myapp
```
will update the remote code (deploy) the app.

* the command:
```
python dev_appserver.py myapp
```
*myapp* maps the name in the [app.yaml](https://developers.google.com/appengine/docs/python/config/appconfig) file. `dev_appserver.py` command will look into `app.yaml` entries.

App Engine will perform:
1. check the `app.yaml` for the main file
2. read the code in the main file

You local server is up, and will respond to request at http://localhost:8080

## Inside the App

`main.py` is the entry-point of the app (as written in the `app.yaml`). The file where any behaviour of the program is defined.
This is a skeleton app:

```
# Import Libraries
import webapp2
from google.appengine.ext.webapp import template
import os.path

# Method In The Wild
def render_template(self, view_filename, params=None):
        if not params:
          params = {}
        path = os.path.join(os.path.dirname(__file__), '../../views', view_filename)
        self.response.out.write(template.render(path, params))

# Handler        
class Index(webapp2.RequestHandler):
    def get(self):
       return render_template('index.html')

app = webapp2.WSGIApplication([
    # Definition Of Routing
    webapp2.Route('/', Index)
], debug=TRUE)

```

This short introduction let us experience what is the flow from/to the App Engine instance.
As we said, once you uploaded the code it will be hosted and served by Google inside the App Engine PaaS.

If you start the development server, it is served locally, only for you to access and test the code.

When you app url is inquired, locally or remotely:

1. A **client** (usually a browser) send a request to a **server** pointing the server's URL.
2. The server receives the request and passes it to the app **dispatcher** (in our case the webapp2's dispatcher)
3. The dispacher, through its libraries, check the **routing** of the app. The section 'Definition Of Routing' is a mapper of URI to **handlers**
4. The routing asks a **handler** (a Python class in this case) to start the computation to respond the request
5. The handler does its job and respond properly (in our case with a **template** page)
6. Hopefully the user gets what he/she asked for on his/her browser window





Python console 

Creating a Python module

Python in App Engine

Hello World App Engine
