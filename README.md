# Dailytask1
Daily task given in zen portal this taks is about difference between htpp 1.1 and http 2.0 and object and its internal representation
Question 1

Write a blog on Difference between HTTP1.1 vs HTTP2
Introduction:
The Hypertext Transfer Protocol (HTTP) is the foundation of communication on the World Wide Web. Over time, this protocol has undergone significant improvements to enhance web performance, resulting in the development of HTTP/2. In this blog post, we will explore the key differences between HTTP/1.1 and HTTP/2 and understand how the latter has revolutionized web browsing.

Request-Response Mechanism:
HTTP/1.1: In HTTP/1.1, multiple requests were processed sequentially over a single connection. The server had to respond to each request before moving on to the next one. This created a potential bottleneck and led to a delay in loading web pages.
HTTP/2: HTTP/2 introduced a new multiplexing mechanism, allowing multiple requests and responses to be processed simultaneously over a single connection. This improved performance by eliminating the need for multiple connections and minimizing latency. The multiplexing feature enables efficient resource utilization, resulting in faster page loads.

Header Compression:
HTTP/1.1: Each request and response in HTTP/1.1 included headers, which contained metadata about the request or response. However, these headers were sent as plaintext, resulting in redundant information being transmitted with each request. This increased the size of the payload and negatively impacted performance.
HTTP/2: HTTP/2 employs a technique called header compression using the HPACK algorithm. It compresses header information before transmission, significantly reducing overhead and improving network utilization. By compressing headers, HTTP/2 reduces the amount of data that needs to be transferred, leading to faster communication between the client and the server.

Server Push:
HTTP/1.1: In HTTP/1.1, the client had to make individual requests for each asset required to render a web page. This often led to the server responding with multiple round trips to fetch additional resources, resulting in increased latency and slower page loads.
HTTP/2: HTTP/2 introduced the server push feature, which allows the server to proactively send assets to the client before they are requested. This optimization eliminates the need for additional round trips, reduces latency, and accelerates the page rendering process. Server push enables faster loading times for subsequent pages as well, as the server can anticipate the required resources.

Stream Prioritization:
HTTP/1.1: Requests in HTTP/1.1 were processed in the order they were sent, without considering their relative importance. This lack of prioritization meant that critical resources, such as stylesheets or scripts, were treated the same as less important ones, leading to suboptimal performance.
HTTP/2: HTTP/2 introduced the concept of stream prioritization, allowing the client to assign weights and dependencies to requests. This enables the browser to prioritize the delivery of critical resources, enhancing page rendering speed. By intelligently prioritizing streams, HTTP/2 ensures that essential assets are loaded first, resulting in a smoother user experience.

Question 2

Write a blog about objects and its internal representation in Javascript

Introduction:
In JavaScript, objects are fundamental entities that allow developers to represent and manipulate data in a structured manner. Behind the scenes, JavaScript employs a sophisticated internal representation for objects, which plays a crucial role in how they are stored, accessed, and manipulated. In this blog post, we will delve into the internal representation of objects in JavaScript, shedding light on their underlying mechanisms.

Properties and Methods:
In JavaScript, objects consist of properties and methods. Properties are used to store data, while methods are functions associated with objects that perform actions or computations. Internally, JavaScript represents properties and methods as key-value pairs within an object's internal data structure.

Object Creation:
There are multiple ways to create objects in JavaScript, including object literals, constructor functions, and classes. Regardless of the creation method, objects in JavaScript are ultimately represented as instances of the Object class. The internal representation of an object includes a hidden internal property called [[Prototype]], which references the object's prototype.

Prototypes and Prototypal Inheritance:
Prototypes play a fundamental role in JavaScript's object model. Each object in JavaScript has a prototype, which is essentially another object. When accessing a property or method of an object, JavaScript checks if it exists directly on the object. If not, it looks up the prototype chain until it finds the property or encounters the end of the chain. This mechanism is known as prototypal inheritance.

Object Descriptors:
JavaScript provides Object.defineProperty() and Object.defineProperties() methods to define properties with additional characteristics, known as descriptors. Descriptors allow developers to specify attributes like configurability, enumerability, writability, and getter/setter functions for properties. These descriptors are stored as part of an object's internal representation.

Property Access and Lookup:
When accessing a property of an object, JavaScript follows a series of steps to determine the value to be retrieved. It first checks if the property exists directly on the object itself. If not found, it traverses the prototype chain until it locates the property or reaches the end of the chain. This process, known as property lookup, leverages the internal [[Prototype]] link between objects.

Object Shape and Hidden Classes:
JavaScript engines optimize object access and manipulation by employing hidden classes. When an object is created, JavaScript assigns it a hidden class that defines its shape, including the arrangement of properties and their types. This allows the engine to optimize property access by assuming objects with the same hidden class have similar layouts, resulting in faster property lookups.

Garbage Collection:
JavaScript employs automatic garbage collection to manage memory. When an object is no longer referenced, it becomes eligible for garbage collection. The internal representation of objects includes mechanisms to track object references and perform garbage collection when necessary, freeing up memory resources.
