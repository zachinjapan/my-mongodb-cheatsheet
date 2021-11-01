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


