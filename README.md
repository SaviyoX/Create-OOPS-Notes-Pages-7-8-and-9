Here in the above example, we considered a void method rank points. This method is a void method, which doesn't return any value. The call to a void method must be a statement.

Passing Parameters by Value.
While working under calling process, arguments is to be passed. these should be in the same order as these respective parameters in the method specifications. parameters can be passed by value or by reference.
Passing parameters by value means calling a method with a parameter. through this the argument value is passed to the parameter.
 Eg: the following pgm shows an egL of passing parameter by value. the values of the arguments remains the same even after the method invocation.

Public class swapping

{  
public static void main(String args[])
		{
    int a=30, b=45;
		  System.out.println("Before swapping a= " + a + "and b= " + b);
		  Swapfunction (a,b);
		  System.out.println("In After Swapping, a + " + a + " and b = " + b);
		}
	Public static void swapfunction(int a, int b)
		{ System.out.println("Before swapping(inside function), a = " +a+"b= " + b);
		 int c =a;
		 a=b;
		 b=c;
		 System.out.println("After swapping(Inside function)a = "+a+" and b= "+b);
		}
Output:
Before swapping a = 30 and b= 45
before swapping (inside function) a =30 and b=45
after swapping (inside function) a =45 and b=30
after swapping a=30 and b = 45


Access Modifier in Java.
There are two types of modifiers in Java access modifiers and Non-Access Modifiers. The access modifier in Java, specifies scope of a data member, method constructor  or class. there are 4 types of Java Access modifiers.
(I) Private Access Modifier: The Private A.M. is accessible only within class.
eg: class A
	{ private int data=40;
	 private void msg()
		{ System.out.println("Hello")};
	}
Public class Sample
	{Public static void main(Strings args[])
		{ A obj = new A(); //Object creation syntax
		 System.out.println(obj.data); //compile time error 
		 obj.msg(); //compile time error
		}
	}


We have created two classes A and sample. the class A contains private data member and private method. we are accessing these private members from outside the class. so, there is compile time error.

(ii) default A.M.
	If you do not use any modifier it is treated as default. the default modifer is accessible only within package.
eg: A.java (saved by)

Package pack:
class A
	{void msg()
		{System.out.println("Hello");}
	}
B.java
Package mypack;
import pack*;
class B
{
	public static void main(String args[])
	{
		A obj = new A(); // compile time error
		obj.msg();// compile time error
	}
}

In this example we have created two packages pack and mypack. we are accessing the class A from poutside its package. since a class is not public, so it cannot be accessed from outside the package. The scope of class a and its method msg() is default. So it cannot be accessed from outside the package.

(iii) Protected A.M.
	This is accessible within ppackage and outside the package, but throught inheritance only. The protected A.M. can be applied on the data member, method and contructor. It cannot be applied on the class.
eg: A.java
Package pack;
Public class A
	{protect void msg()
		{System.out.println("Hello")};
	}

B.Java
Package mypack;
import pack*;
classB extends A
{public static void main(String args[])
	{B obj = new B();
	 obj.msg();
	}
}

O/P

Hello

We have created two packages pack and my pack. The class A of 'pack' package is public, so can be accessed from outside the package. But msg() method of this package is declared as protected. So it can be accessed from outside the class only through Inheritance.
