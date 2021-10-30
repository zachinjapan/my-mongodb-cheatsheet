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
mongoImport

mongorestore

```
# Export
```
mongoDump -- uri  <atlas cluster URI>
exports data in BSON

mongoexport --uri uri  <atlas cluster URI>
            --collection = <collection name>
            --out=<filename>.json
exports data in JSON

```
