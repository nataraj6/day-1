1-question
Write a blog on Difference between HTTP1.1 vs HTTP2 ?
HTTP1.1
1.It supports connection reuse i.e. for every TCP connection there could be multiple requests and responses, and pipelining where the client can request several resources from the server at once. However, pipelining was hard to implement due to issues such as head-of-line blocking and was not a feasible solution.
2. Expands on the caching support by using additional headers like cache-control, conditional headers like If-Match and by using entity tags.
3. It is relatively secure since it uses digest authentication, NTLM authentication
4. Introduces a warning header field to carry additional information about the status of a message. Can define 24 status codes, error reporting is quicker and more efficient.

HTTP2
1.Uses multiplexing, where over a single TCP connection resources to be delivered are interleaved and arrive at the client almost at the same time. It is done using streams which can be prioritized, can have dependencies and individual flow control. It also provides a feature called server push that allows the server to send data that the client will need but has not yet requested.
2.HTTP/2 does not change much in terms of caching. With the server push feature if the client finds the resources are already present in the cache, it can cancel the pushed stream.
3.Security concerns from previous versions will continue to be seen in HTTP/2. However, it is better equipped to deal with them due to new TLS features like connection error of type Inadequate_Security.
4.Underlying semantics of HTTP such as headers, status codes remains the same.




2-question
Objects and its internal representation in Javascript  ?



1.Object:
In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

Creating Objects in JavaScript:

1.By object literal
2.By creating instance of Object directly (using new keyword)



By object literal:

The syntax of creating object using object literal is given below:


object={property1:value1,property2:value2......propertyN:propertyN}

Property and value is separated by colon(:).

Example:

var=person{
fname:"xxx",
lname:"yyy"
age:25
};

	
	
	
By creating instance of Object directly (using new keyword):



The syntax of creating object directly is given below:


var objectname=new object();


Here, new keyword is used to create object.

Example:
       var emp=new object();
			 emp.id=101;
			 emp.name=:"xxx"
        emp.salary=50000
				
				
				
				
Accessing JavaScript Objects:


The syntax for accessing the property of an object is:


objectName.property

or

objectName[“property”]

Accessing ‘fname’ from example 1 using dot operator,
  person.fname

Accessing ‘name’ form example 2 using [],


emp["name"]
