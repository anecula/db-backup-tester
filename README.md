# db-backup-tester
ansible will be used to:  
1. set up a new instance in EC2 AWS  
2. install msql, aws client  
3. copy the script that will test the backups  
4. run the script   

build the sh script that will do:  
- cycle through a configurable number of buckets  
- for each bucket is a folder per machine (only on live machines)  
- in each folder is one folder per date, only the last x days will be tested (x is configurable in the script)  
- in each date folder is one file per data base  
- the script will download all the archives and will load them on the mysql server  
- if at leat one DB restauration fails the hole day is marked as failed  
- all the info will be added to a log  
- at the end of the script the log will be send to a configurable email address 
