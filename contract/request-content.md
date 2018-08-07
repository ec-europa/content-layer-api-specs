# Get Content

## parameters

```javascript
"triples":[
  {
  "subject": ["http://schema.org/GovernmentOrganization"];
  "predicate": ["https://schema.org/name"];
  "object": ["DGCOMM"];
  }
]
```

## query

```javascript
  {
    GetLinkedDataFragment($triples){
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
