# Welcome

MRML (pronounced "murmel") is designed to express how various parts of a model railway link together in an easy to read format for both humans and machines

## Examples

Let's get started straight away with a very simple example.

In this case, we're creating a section of track that comprises three blocks based (Very losely!) on part of the St. Ives Branchline in Cornwall, UK:

```yaml
---
# SimpleLayout.mrml
layout:
  name: "St Ives Branchline"
  blocks:
    - name: "Carbis Bay"
      terminus: True
      up_line: "Branch Line"
      down_line: None
    - name: "Branch Line"
      terminus: False
      up_line: "Carbis Bay"
      down_line: "St Ives"
    - name: "St Ives"
      terminus: True
      up_line: "Branch Line"
      down_line: None
```

This example provides us with three track blocks that we can bring into our layout automation, along with the connections of where traffic has come *from* (`up_line`) and where the traffic is expected to go *to* (`down_line`), giving us a really simple layout that effectively looks like `Carbis Bay <-> Branch Line <-> St Ives`.

Explore the documentation further to see how you can express different types of track sections such as turnouts and sidings, use metadata to associate blocks on your layout with sections on the real-life railways, and use MRML to automate your layout.

## Why did you do this?

I spend my days writing YAML to describe everything from application configuration to launching thousands of servers in cloud environments and stating how they should be monitored.  It made sense to me to come up with an easy to learn, interchangable format based on YAML that could be used to describe how my layout fitted together so I could then write other tools that would automate my layout based on the content of my MRML files.
