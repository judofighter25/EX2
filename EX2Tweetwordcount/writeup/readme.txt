
#Below is the instructions on how to run my code for EX2.
#Step 1
#Setting Up Postgre SQL tcount database and tweetwordcount table. 
#Please highlight all the line below, copy, then paste it 
#into terminal.  It will setup the database and table in Postgre

psql -U postgres
drop database tcount;
create database tcount;
\l
\c tcount
create table tweetwordcount (word varchar(100), count integer);
select * from tweetwordcount;
\q



#Start Storm process
#Once all the files are uploaded to the Storm structure change to the storm directory: 
# $ cd EX2Tweetwordcount
# In EX2Tweetwordcount directory: sparse run


#Storm streaming
#Once Storm streaming process starts, it will stream data from Twitter feeds.
#Word count calculations will be performed then updated to Postgre table tweetwordcount in 
#tcount database.
#Please manually stop the process with Control + C otherwise the whole process will
#continue to run.

#Query data from Postgre 
#finalresults.py and histogram.py files can be found under EX2Tweetwordcount directory.
#Start finalresults.py: python finalresults.py <word>  Please put a space between .py and <word>
#Start histogram.py: python histogram.py <number1>  <number 2>  Please put space between 
#<number 1> and <number 2> ; no comma or additional symbols between <number 1> and <number 2>.

 