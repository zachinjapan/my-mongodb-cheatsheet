# my-mongodb-cheatsheet

## Show All Databases

```
show dbs
```

## Show Current Database

```
db
```

## Create Or Switch Database

```
use <database name>
```

## Importing and Exporting


# Import
```
mongorestore --uri "<Atlas Cluster URI>"
            --drop dump
imports data in BSON dump

mongoImport  --uri "<Atlas Cluster URI>"
             --drop=<filename>.json
             
imports data in JSON

```
# Export
```
uri = uniform resource identifier

mongoDump -- uri  <atlas cluster URI>

/exports data in BSON

mongoexport --uri <atlas cluster URI>
            --collection = <collection name>
             --out=<filename>.json
            
/exports data in JSON

```

## find

```
db.<collection>.find({key and value}) 
if you want it pretty add .pretty()
if you want the count add .count();
```


## adding documents to collection

```
db.<collection>.insert([{ "_id": 1, "test": 1 },{ "_id": 3, "test": 3 }])
```


## updating documents to collection

```
updateOne()
updates only one of many possible matches
updateMany()

$inc
db.<collection>.updateMany({ "city": "HUDSON" }, { "$inc": { "pop": 10 } })
$set
db.zips.updateOne({ "zip": "12534" }, { "$set": { "population": 17630 } })
$push
```
## push vs set

```
For $set, you are able to set a specific element in the array. For $push it will always be at the end.

For $set, using the array dot notation might cause unexpected result when the given element does not exists. Because $set will not create an array field but an object field. For example, if you do

```

## deleting documents

```
db.<collection>.deleteOne({info})

db.<collection>.deleteMany({info})

```
