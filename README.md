# mongodb.json - App success made simple
# fast database with json extends mongoose style

# Installing

```bash
$ npm init
$ npm install --save mongodb.json
```

# fast database with json extends mongoose style

#setup
```js
 const mongooseJson = require("mongodb.json") // mongooseJson it is the class of the package
 
 const usersSchema = { // normal javascript object and its the schema
    name: String, // String it is the type of the key
    age: Number, // Number it is the type of the key
    nickname: String, // String it is the type of the key
    password: String || Number 
}

const usersModel = new mongooseJson({
 path: "database.json" // its the file name
 dir: "database" // the dir of database.json file
}, usersSchema /* schema varible*/ ) 
```

# how to create a new Data

```js
async function createData() {
 const data = usersModel.create(d => d.name = "hello") // -> {"name": "hello"}
}
```
# how to find Data

```js
async function findData() {
 const data = usersModel.findOne({name: "hello"}) 
 console.log(data) // -> {"name": "hello", id: "......"}
}
```
# how to edit or add property

```js
async function save() {
 const data = usersModel.findOne({name: "hello"}) 
 data.name = "ziad"
 data.password = 13313193201e
 data.nickname = "ziath"

 data.save()
}
```

# how to delete data

```js
async function delete() {
 const data = usersModel.findOne({name: "hello"}) 
 data.delete()
}
```

# all current methods 

| methods      | Description |
| ----------- | ----------- |
| findOne     | find element|
| create      | create new Object|
| fetch       |get all data|
|findOneOrCreate| soon...|

# dev

```bash
Ziath#1768
```
