---
layout: post
title:      "Key Ruby concepts explained. "
date:       2020-04-23 12:19:13 -0400
permalink:  key_ruby_concepts_explained
---

In this blog I will be going over a few key concepts of Ruby that I have been struggling to grasp thus far. These concepts are class and instance methods, class and instance variables, iterators and implicit return. 

A **Class Method** is a method that is defined on the class. It provides functionality to the class itself. Like this 

```
class Basket  
def self.find(id)  
puts "finding basket with the id of #{id}"  
end  
end  
```

In this example I’ve used self in the method. This is signifying that this method is a class method. You should use class methods when the functionality you are writing does not belong to an instance of that class.

A **Instance Methods** on the other hand, can only be called on an instance of the class. It provides functionality to one instance of a class.

```
class Basket  
def self.find(id)  
puts "finding basket with the id of #{id}"  
end

def products  
[]  
end  
end   
```

In this example I’ve added a products instance method. This instance method only makes sense when we actually have an instance of the basket class.

Instance Methods should be used when you need to act on a particular instance of the class. For example, the products method only makes sense in the context of a Basket instance. You can’t have a list of products without actually having a basket object to work with.

**Class variables** are shared by all objects of a class and always start with the @@ symbols.
 

**Instance variables** are variables that are dependent or tied to one object. And always start with @ symbols.


```
class Customer 
      
# class variable
 @@num_of_customers = 0
   
 def initialize(id, name, addr) 
       
# An instance Variable 
 @cust_id = id
 @cust_name = name 
 @cust_addr = addr 
 end
   
 def total_num_of_customers() 
       
# class variable 
 @@num_of_customers += 1
 puts "Total number of customers: #@@num_of_customers"
    end
end
``` 
     
In the code snippet above we have a Customer class. In this customer class we have a class variable its value is shared by all objects created from the Customer class.

The instance variable is different from each object created from the class. Each customer has a name, address or a instance of the customer class.

**Iterators** - iterators are methods that are supported by collections like arrays and hashes.
`.each` would be used if you wanted to return the original array. `.map` would be used if you wanted to return a modified array. A block is a piece of code that accepts arguments, and returns a value. It can be put inside do and end or { } for one-liners.

**implicit return** will return the value of the last line automatically doing away with the `return` keyword. On the other hand **explicit return** can be used if you dont want to return the last line of code, you can explicitly tell ruby to return apple instead of orange like this.
```
return apple - Explicit return
       orange - Implicit return
``` 				 

These key concepts are key for me because they are ones that I have struggled with, and being able to write them out really helped me clear up any confusion that I still had.  


