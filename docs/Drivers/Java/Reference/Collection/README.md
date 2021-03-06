# Collection API

These functions implement the
[HTTP API for collections](https://docs.arangodb.com/latest/HTTP/Collection/index.html).

The _ArangoCollection_ API is used for all collections, regardless of
their specific type (document/edge collection).

## Getting information about the collection

See
[the HTTP API documentation](https://docs.arangodb.com/latest/HTTP/Collection/Getting.html)
for details.

## ArangoCollection.exists

```
ArangoCollection.exists() : boolean
```

Checks whether the collection exists

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
ArangoCollection collection = db.collection("potatos");

boolean exists = collection.exists();
```

## ArangoCollection.getInfo

```
ArangoCollection.getInfo() : CollectionEntity
```

Returns information about the collection.

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
ArangoCollection collection = db.collection("potatos");

CollectionEntity info = collection.getInfo();
```

## ArangoCollection.getProperties

```
ArangoCollection.getProperties() : CollectionPropertiesEntity
```

Reads the properties of the specified collection.

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
ArangoCollection collection = db.collection("potatos");

CollectionPropertiesEntity properties = collection.getProperties();
```

## ArangoCollection.getRevision

```
ArangoCollection.getRevision() : CollectionRevisionEntity
```

Retrieve the collections revision.

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
ArangoCollection collection = db.collection("potatos");

CollectionRevisionEntity revision = collection.getRevision();
```

## ArangoCollection.getIndexes

```
ArangoCollection.getIndexes() : Collection<IndexEntity>
```

Fetches a list of all indexes on this collection.

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
ArangoCollection collection = db.collection("potatos");

Collection<IndexEntity> indexes = collection.getIndexes();
```
