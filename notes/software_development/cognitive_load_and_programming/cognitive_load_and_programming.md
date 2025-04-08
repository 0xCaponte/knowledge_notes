
# Cognitive Load and Programming

Source: minds.md/zakirullin/cognitive

- Cognitive Load is how much we need to think to understand and complete a task

- We have limited working memory: The more there is to keep in mind, the higher the load and the confusion.

- Tasks have an inherit complexity, nothing we can do about that part. But we can **reduce the extra complexity** surrounding them.

Examples of extra complexity:

 - Ifs with multiple complex conditions
 - Complex Inheritance
 - Global Variables updated in different places
 - Shallow and non-descriptive methods
 - Many concatenated methods, or method calls used as parameters
 - Too many dependencies with little use 

Example:

- Complex: 

		if (condition1 && (condition2 || condition3) && (!condition4 || condition5)) 

- Clearer Options:

   	- Nested Ifs
    
	    	if (condition1){

	    		if (condition2 || condition3) {
	    			.
	    			.
	    			.
	    		}    	
	    	} 

    - Intermediate variables for the conditions

	    	isActive = condition2 || condition3
	    	isPresent = !condition4 || condition5

	    	if (condition1 && isActive && isPresent) { 

	    	}

- Abstraction & Methods should hide complexity not simply redirect it or split it.

- **Smart and clever implementations usually make things more complex for anyone not familiar with that decision. That clever trick is something else to learn and keep in mind. Is it really needed?** 

	Being familiar with the code doesn't mean it is clear or well written, just that you currently know your way around your mess


**>> This way you might end up with "stupid" looking code, but a code that people can work with. <<**