# Data Modeling Notes

## Requirements

A client has hired you to build an API for managing `zoos` and the `animals` kept at each `zoo`. The API will be use for `zoos` in the _United States of America_, no need to worry about addresses in other countries.

For the `zoos` the client wants to record:

- name.
- address.

For the `animals` the client wants to record:

- name.
- species.
- list of all the zoos where they have resided.

Determine the database tables necessary to track this information.
Label any relationships between table.

## A good data model

- captures ALL the info the system needs
- captures ONLY the info the sys needs
- relfect reality (from the point of view of the system)
- is flexible, can evolve with the system
- guarantees `data integrity`, without sacrificing too much performance.
- is driven by the way we access data.

## Components of a data model

- entities 
    (nouns: zoo, animal, species), like a resource --> map to tables
- properties
    ---> columns or fields
    - relationships --> Foreign keys (FK)

## Workflow

- identify entities
- id the properties
- id relationsships

## Relationships

- one to one
- one to many: this is the most common!
- many to many: this is smoke an mirrors.

_...there are many animals in one species_
_...there can be more than one animal in a zoo_
_...an animal could have lived in more then one zoo_

## Mantras

- Every table must have a **Primary Key**
- Work on **two or three entities** at a time
- **one to many** are modeled using **FK**
- the **FK** always goes on the many side
- the for **FK Colum** must be the **same type** as the **PK** it references.
- **many to many** relationships are modeled using a **third table**
- the third table could include other columns