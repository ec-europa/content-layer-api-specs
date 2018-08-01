# Get Department by name

The power of triples

> Mike → said → (triples → can be → objects)

## parameters

```javascript
{
"subject": ["Department"];
"predicate": ["name"];
"object": ["DGCOMM"];
}
```

## query

```javascript
{
  Department_GET_BY_NAME(names:$object){
    // properties
    _id
    _type
    name(lang:"en")
    description
  }
}
```

```javascript
  {
    GetLinkedDataFragment(
      subject: $subject
      predicate: $predicate
      object: $object
    ){
      // properties
      _id
      _type
      name(lang:"en")
      description
    }
  }
```

## response

```javascript
{
    "@context": {
      "name": "http://schema.org/name",
      "description": "http://schema.org/description",
      "xsd": "http://www.w3.org/2001/XMLSchema#"
    },
    "name": "DGCOMM",
    "description": "some blurb",
}
```
