# drf-relation-id

Autmoatically add `"_id"` to [DRF](http://django-rest-framework.org)
relationship fields when serializing.

This code has been extracted from https://github.com/ostcar/OpenSlides
The original (MIT) license has been retained.

# Example

## Serializer
```
from drf_relation_id import IdModelSerializer
import models

class ChildSerializer(IdModelSerializer):
  class Meta:
    model = models.Child
    fields = (
        'id',
        'parent', # ForeignKey
    )
```

## Serializer output
```
{ id: 1, parent_id: 1 }
```
