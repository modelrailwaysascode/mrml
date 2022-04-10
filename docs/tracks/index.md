# Tracks

A track is the primary unit within MRML.

Tracks are expected to at least have a name and details of where they connect to or if they are a terminus block.

Metadata can be assigned to a track to enhance the details available.

## Full Track Description

The following details an entire track section with all available options:

```yaml
---
tracks:
  - name: My First Track Block
    up_line: None # The preceeding track in the direction of travel
    down_line: My Second Track Block # The following track in the direction of travel
    terminus: True # Is this block a terminus or not? This could be a head-shunt, siding, platform, or other such area
    metadata:
      description: A random description # A string of text that could describe the track
```
