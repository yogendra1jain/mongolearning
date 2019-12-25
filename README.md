Replica Set- 

1.Create folder replica in which crate 3 folders db1,db2,db3 start a cmd here 
2.Type command mongod --dbpath D:\repliccaset\db1 --replSet NAVREplica
3. mongod --dbpath D:\repliccaset\db1 --replSet NAVREplica --port 27018
4. mongod --dbpath D:\repliccaset\db1 --replSet NAVREplica --port 27019

5.Create a configuration obj 

var configuration = {
_id:"NAVREplica",
members : [
{_id:1,host:"localhost:27017"],
{_id:1,host:"localhost:27018",slaveDelay:20,priority:0],
{

6.connect to mongo client 27017

7. set configuration variable (copy paste step 5 in console)

8.rs.initiate(configuration) 

9. we can enaable reading from secondary server by writing command rs.slaveOK(true)

One server will start as primary and others will be secondary
