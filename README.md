# Ruby Bug: Instance Variable Modification

This repository demonstrates a common, yet subtle, bug in Ruby code where directly modifying instance variables using `instance_variable_set` can lead to unexpected behavior.  This can make code difficult to debug and maintain.  The solution shows a safer, more maintainable approach.

## Bug
The `bug.rb` file showcases the issue.  It involves a class with a getter method for an instance variable. Modifying the instance variable directly using `instance_variable_set` bypasses the getter method's potential logic, leading to unexpected results if the getter had any extra functionality beyond simple access.

## Solution
The `bugSolution.rb` file provides a solution that avoids direct modification of instance variables. Instead, it uses a setter method that maintains encapsulation and allows for controlled modification of the instance variable. This makes the code more robust and maintainable.