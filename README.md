use myDatabase
< switched to db myDatabase
...
> show databases
Search connections
< Company_DB 116.00 KiB
admin 40.00 KiB
localhost:27017
config 108.00 KiB
£ Company_DB
local 88.00 KiB
Employee
myDatabase 36.00 KiB
employee
> show collections
staff
myCollection
> db.myCollection. insertOne({"name":"a","age:":30, "address :""udupi"})
admin
SyntaxError: Unexpected token (1:58)
*[Om[31m[1m>[22m[39m[90m 1|[39m db[33m.[39mmyCollection[33m.[39minsertOne({[32m"name"[39m[33m:[39m[32m"& myDatabase図[90m[39m
> db.myCollection. insertOne({"name":"a","age:":30, "address": "udupi"})
acknowledged: true,
insertedId: ObjectId('682bc84915c9fa923cf1ecd8')
> db.myCollection. insertOne({"name":"a","age":30,"address":"udupi"})
acknowledged: true,
insertedId: ObjectId('682bc91015c9fa923cf1ecd9')
> db.myCollection. insertMany([{"name":"a","age":30, "address": "udupi"}, {"name" : "b", "age": 30, "address": "karamballi"}])
acknowledged: true,
insertedIds: {
'0': ObjectId('682bc9bc15c9fa923cf1ecda'),
'1': ObjectId('682bc9bc15c9fa923cf1ecdb')
> db.myCollection. find([{"name":"a","age":30,"address":"udupi"})
« SyntaxError: Unexpected token, expected "," (1:61)
[Om[31m[1m>[22m[39m[90m 1|[39m db[33m.[39mmyCollection[33m.[39mfind([{[32m"name"[39m[33m:[39m[32m"a"*[
X[90m|M [39m*[31m[1m^*[22m[39m[0m
> db.myCollection. find({"name": "a", "age":30, "address":"udupi"})
_id: ObjectId('682bc91015c9fa923cf1ecd9'),
name: 'a',
age: 30,
address: 'udupi'
_id: ObjectId('682bc9bc15c9fa923cf1ecda'),
name: 'a',
age: 30,
address: 'udupi'
> > db.myCollection.find()

_id: ObjectId('682bc84915c9fa923cf1ecd8'),
name: 'a',
'age:': 30,
address: 'udupi'

_id: ObjectId('682bc8755b7fc3013311b47a'),
name: 'John Doe',
age: 30,
email: 'john.doe@example.com'

_id: ObjectId('682bc91015c9fa923cf1ecd9'),
name: 'a',
age: 30,
address: 'udupi'

_id: ObjectId('682bc9bc15c9fa923cf1ecda'),
name: 'a',
age: 30,
address: 'udupi'
>_MONGOSH
name: 'a',
age: 30,
address: 'udupi'

_id: ObjectId('682bc9bc15c9fa923cf1ecda'),
name: 'a',
age: 30,
address: 'udupi'

_id: ObjectId('682bc9bc15c9fa923cf1ecdb'),
name: 'b',
age: 30,
address: 'karamballi'

> db.myCollection. findOne()

_id: ObjectId('682bc84915c9fa923cf1ecd8'),
name: 'a',
'age:': 30,
address: 'udupi'

> db.myCollection. findOne(a)
" ReferenceError: a is not defined
myDatabase> db.myCollection. findOne(a)
> db. ["myCollection"]. find()
« SyntaxError: Unexpected token (1:3)

[Om[31ml [1m>[22m[39m[90m 1 |[39m db[33m.[39m[[32m"myCollection"[39m][33m.[39mfind()×[90m| [39m[31m [1m^k[22m [39ml [om
