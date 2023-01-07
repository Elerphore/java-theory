# Java interview questions:


## JUNIOR

* ### What is JIT?
	* Compiles bytecodes to machine code at run time.
	* Just in time compiler. Part of the JRE, that is responsible for perfomance optimization of java based applications at run time.
	* The JIT compiler aids in improving the perfomance of Java programs by compiling bytecode into native machine code at run time.
	* It can affects startup time of application, even if in the end result is a very good perfimance optimization.
	* Optimizations list:

		|                       |                               													 |
		|-----------------------|------------------------------------------------------------------------------------|
		|Dead Code		 		|`Removing code which is not used`													 |	
		|Escape analysis 		|`Moving objects created in methods and never returned, to stack instead of the heap`|
		|Loops           		|`Combining loops, unrolling loops, loop inversion etc`								 |
		|Method inlining 		|`Moving bodies of small methods withing the calling methods`						 |
		|Lock removal    		|`Of only 1 thread every uses the lock, remove it`									 |
		|Null check elimination |`If variable is nevel null, remove the null check code`							 |

	* #### Links:	
		* https://www.youtube.com/watch?v=sJVenujWGjs
		* https://www.geeksforgeeks.org/just-in-time-compiler/

* ###  What is a ClassLoader?
	* Java ClassLoader is a part of the JRE that dynamically loads Java classes into the JVM.
	* Because of that Java Runtime doesn not need to know about files and files systems.
	* Java classes aren't loaded into memory all at once, but they when required by an application. At this point, the Java ClassLoader is called by the JRE and these ClassLoaders load classes into memory dynamically.
	* There's multiple classloaders for java classes:
		* Bootstrap ClassLoader (Primordial ClassLoader)

			A Bootstrap ClassLoader is a machine code which kickstarts the operation when the JVM calls it. It's not a java class. Its job to load first pure Java ClassLoader. Bootstrap ClassLoader loads classes from the location rt.jar. Bootstrap ClassLoader doesn't have any parent ClassLoaders.

		* Extension ClassLoader

			The Extension ClassLoader is a child of Bootstrap ClassLoader and loads the extensions of core java classes from the respective JDK Extension library. It loads files from jre/lib/ext directory or any other directory pointed by the system property *java.ext.dirs*.

		* System ClassLoader (Application ClassLoader)

			An Application ClassLoader. It loads the application type classes found in the environment variable CLASSPATH, -classpath or cp. The Application ClassLoader is a child class of Extension ClassLoader.

	* ClassLoader hierarcy
		* Application ClassLoader -> Extension ClassLoader -> Bootstrap Class loader.
		* The Bootstrap ClassLoader is always given the higher priority, next is Extension and the Application ClassLooaders.
	* The very first class in the application is loaded by using the static main method. From that all the others classes will be loaded as required by this particular class.
	* #### Links:	
		* https://www.youtube.com/watch?v=S7whKuAvRBU
		* https://www.geeksforgeeks.org/classloader-in-java/
		
* ###  What are the memory allocations available in Java?
* ###  Will the program run if I write static public void main?
* ###  What is the default value stored in local variables?
* ###  What is the output of the following code segment?
* ###  What is an Association?
* ###  Define copy constructor in Java
* ###  What is a Marker Interface?
* ###  What is object cloning?
* ###  Why is Java not completely object-oriented?
* ###  Define wrapper classes in Java
* ###  Define singleton classes in Java
* ###  Define package in Java
* ###  Can you implement pointers in a Java program?
* ###  Differentiate between instance and local variables
* ###  Explain Java string pool
* ###  What is an Exception?
* ###  What is a final keyword in Java?
* ###  What happens when main() isn't declared as static?

## MIDDLE

* ### What is JDK?
* ### Brief Access Specifiers and Types of Access Specifiers.
* ### Can a constructor return a value?
* ### Explain "this" keyword in Java
* ### Explain super keyword in Java
* ### Explain Method Overloading in Java.
* ### Can we overload a static method?
* ### Define Late Binding
* ### Define Dynamic Method Dispatch
* ### Why is delete function faster in linked list that array?
* ### Give a briefing on the life cycle of a thread.
* ### Explain the difference between >> and >>>
* ### Brief the life cycle of an applet
* ### Why are generics used in Java.
* ### Explain Externalizable interface.
* ### Explaim Daemon Thread
* ### Explain the term enumeration in Java
* ### Why is Java is Dynamic in nature
* ### Can you run a code before executing main method?
* ### How many times the finalize method called?

## ADVANCED

* ### Can "this" and "super" keywords be used together?
* ### Exaplin a JSP page.
* ### Explain JDBC
* ### Explain the various directives in JSP.
* ### What are observer and observable classes?
* ### What is session management in java?
