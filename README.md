# Hadoop-Map-Reduce-python-
## "map-reduce code to find how many 1 star, 2 star, 3 star, 4 star and 5 star movies are there in dataset"

### ->language used : python

### ->library : mrjob version 0.6.12

### ->dataset link : movielens.org

### ->dataset name : ml-100k

### ->platform use : Hortonworks sandbox version 2.6.5

### ->others : putty, winSCP

# Steps to execute this project

### step 1:  download the dataset ml-100k from the movielens website.

### step 2:  Extract the dataset in your local machine. our focus is on the file named "u.data".

### step 3:  Launch putty and login to sandbox from this you will land in linux host home directory. here you have to upload/download the dataset file u.data (either            you can use command line of putty or GUI of Ambari to load file in home directory of linux host).

### step 4:  Now we have to upload the dataset file (i.e. u.data) into HDFS using command line or you can use GUI of Ambari.

        Command to upload u.data to HDFS
        
        "hadoop fs -copyFromLocal <local src> <destination path in HDFS>"
        
        "hadoop fs -copyFromLocal u.data ml-100k/u.data"
        
### step 5:  Once you have uploaded the file in HDFS now you in the same way you have to uploaded the code in linux host (you can use winSCP to load the code in                linux localhost file system).
        
### step 6:  Once you have all the file in place, next thing is to run it using Hadoop.

        Command for run the code is:
        
        "python RatingsBreakdown.py -r hadoop --hadoop-streaming-jar <path for hadoop-streaming.jar file> u.data"
        
### step 7:  Enjoy!!
