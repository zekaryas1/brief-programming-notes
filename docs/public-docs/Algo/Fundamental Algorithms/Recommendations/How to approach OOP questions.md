---
date created: Thursday, June 16th 2022, 1:47:45 pm
date modified: Sunday, July 3rd 2022, 11:30:11 am
title: How to Approach OOP Questions
---

# How to Approach OOP Questions

## Handle Ambiguity

- When being asked an object-oriented design question,
	- you should inquire _who _ is going to use it and _how _ they are going to use it.
- Depending on the question, you may even want to go through the "six _Ws":
	- _ who, what, where, when, how, why.

## Define the Core Objects

- Now that we understand what we're designing, we should consider what the “core objects” in a system are.
* For example,
	* suppose we are asked to do the object-oriented design for a restaurant. Our core objects might be things like Table, Guest, Party, Order, Meal, Employee, Server, and Host.

```java
class Guest{

}

class Party{

}

class Meal{

}
...
```

## Analyze Relationships

- Having more or less decided on our core objects, we now want to analyze the relationships between the objects.
- Which objects are members of which other objects? Do any objects inherit from any others? Are relationships many-to-many or one-to-many?
* For example, in the restaurant question, we may come up with the following design:
	* the Party should have an array of Guests.
	* Server and Host inherit from Employee.
	* Each table has one party, but each Party may have multiple Tables .
	* There is one Host for the Restaurant.

```java
class Party{
	Guests[] guests;
}

class Server extends Employee{

}
...
```

## Investigate Actions

- At this point, you should have the basic outline of your object-oriented design. What remains is to consider the key actions that the objects will take and how they relate to each other.
- You may find that you have forgotten some objects, and you will need to update your design.
- Example:
	- Action of Guests include
		- makeOrder()
		- pay()
		- changeTable()
		- callServer()

```java
class Guest{

	public void makeOrder(){
	}
	
	public void pay(){
	
	}
	...
}
...
```
