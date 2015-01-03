#Shell Exercises / Questions

###What tasks would be easier via the command line?  What would be harder?  

###If the command line is/was your primary interface, how does/would it affect your work?  


----------------

##Filesystem Exercises

* Use three different ways to get from `/filesystem/data/backup` to `filesystem/nelle/molecules`.  

* Make a quick diagram of Nelle's directory structure.


-------------


##Creating/Deleting Exercises

* Clean up Nelle's home directory: 
	* move `creatures/`, `molecules/`, `pizza.cfg`, and `solar.pdf` to the `data/` directory.  
	* rename `notes.txt` to `to_do.txt`
	* try to delete `Desktop/`


------------

## New Commands

* echo
* less
* cat
* head
* grep
* wc
* sort

## Task

Find out what this command does generally.  What would this specific command do?  If relevant, what other options are there?  What might you use this for in a research setting?  Write your findings on the etherpad.  

##Quiz

Guess what this does: 

~~~
cut -d , -f 1,5 Analytics_Fall2013.csv
~~~

------------

## Pipe Exercises

* Using what you know so far, write a pipe command that takes our sorted list and returns the LONGEST line length.  There are (at least) two solutions.  

* A file called `animals.txt` contains the following data:

~~~
2012-11-05,deer
2012-11-05,rabbit
2012-11-05,raccoon
2012-11-06,rabbit
2012-11-06,deer
2012-11-06,fox
2012-11-07,rabbit
2012-11-07,bear
~~~

What text passes through each of the pipes and the final redirect in the pipeline below?

~~~
cat animals.txt | head -5 | tail -3 | sort -r > final.txt
~~~

* The command `uniq` removes adjacent duplicated lines from its input.
For example, if a file `salmon.txt` contains:

~~~
coho
coho
steelhead
coho
steelhead
steelhead
~~~

then `uniq salmon.txt` produces:

~~~
coho
steelhead
coho
steelhead
~~~

Why do you think `uniq` only removes *adjacent* duplicated lines?
(Hint: think about very large data sets.) What other command could
you combine with it in a pipe to remove all duplicated lines?

* Challenge for advanced users: The `Analytics_Fall2013.csv` file (in `data/`) contains analytics data from a website.  The first column is a list of URLs and the fifth column is the average time spent on the corresponding webpage.  Write a shell pipeline that extracts pages with "Question" in the URL, and returns the 10 pages with the highest average time on page.  Bonus points for stripping the front of the URL and just leaving the unique page name.  

