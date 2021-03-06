"Context Overload" is a Force.com pattern presented by Richard Vanhook at Dreamforce 2011 during the session titled "Apex Design Patterns and Best Practices".

This patterns defines a way in which to run logic in any context.  The code in this example uses the Metaphone algorithm as a concrete piece of logic.  The basic idea is to consolidate your logic into a single class and allow the logic to be utilized in any context via method overloading.  See Metaphone.cls.

=====================================================
Introduction to Metaphone 
=====================================================
A phonetic algorithm for indexing words by their English pronunciation.  Is used in spell-checkers and search algorithms.

Examples:
Metaphone.calculate('Richard') => RXRT
Metaphone.calculate('Richerd') => RXRT
Metaphone.calculate('Richrd')  => RXRT
Metaphone.calculate('Richrrd') => RXRT

Credits to Kyle Thornton & Cloudspokes for Metaphone algorithm implementation.
 
=====================================================
Pattern Benefits & Tips 
=====================================================
Reuse logic in any of the following contexts:  
	-Execute Anonymous
	-Batch Apex
	-Synchronous Trigger
	-Asynchronous (@future) Trigger
	-Visualforce Controller
	-Scheduled Apex
	-Apex Web Service
Ability to control sharing (with/without) 
Makes code more flexible/reusable
