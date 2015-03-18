Group 10:	David Demeter
		Rahul Matta
		Sachin Lal
		Michael Kushnir
EECS 337-0 Recipe Project

Summary:

Program will parse a given URL into a list of ingredients, including amount, unit of measure, ingredient name(s), description(s), preparation(s) and preparation description(s).  Program will display pare of original recipe in plain English form.  It is also possible to perform one of eight transformations as detailed in the user interface.

Usage:

	python recipe11.py <url> <output filename>

where 
	
	<url> is the http address of a recipe from AllRecipes.com, and
	<output filename> is the path and name where the JSON parse of 
	the original recipe will be saved. 

Dependencies:

The system is comprised of single Python 2.7 file:

	recipe11.py

In addition to the standard Python packages, the system also uses:

	Beautiful Soup 4.2.0 (to facilitate we access), and
	NLTK (to perform some NLP functionality).

The knowledge base used by the program is contained in the following files:

	foods.txt
	desc.txt
	prep.txt
	prepdesc.txt
	tools.txt
	methods.txt
	primary.txt
	ignores.txt

The knowledge base is used by the program to classify tokens in the ingredient and direction lists during the parse of the original recipe.  Regular expressions were applied to any tokens not classified based upon knowledge base.  Transformations are performed using rules and knowledge incorporated in the program code.  Note: Transformed recipes are displayed to the user interface and the JSON parse is not saved to a file.
