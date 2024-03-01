# drf-recursive

## Overview

Recursive Serialization for Django REST framework

This package provides a `RecursiveField` that enables you to serialize a tree,
linked list, or even a directed acyclic graph. Also supports validation,
deserialization, ModelSerializers, and multi-step recursive structures.

## Installation

Install using `pip`...

```bash
$ pip install drf-recursive
```

## Example

```python
from rest_framework import serializers
from drf_recursive.fields import RecursiveField

class TreeSerializer(serializers.Serializer):
    name = serializers.CharField()
    children = serializers.ListField(child=RecursiveField())
```
