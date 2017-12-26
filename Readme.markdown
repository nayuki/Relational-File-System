Relational File System, ongoing development version
===================================================


## Overview

The Relational File System (RelFS) is a proposed new way to store files and represent knowledge.
Although the hierarchical file model is ubiquitous, RelFS is intended complement or replace hierarchies as the preferred way to organize files.

RelFS combines features from classic hierarchical file systems, relational databases, and content-addressable storage systems.
Viewed in another way, RelFS takes the hierarchical model and removes undesirable features and limitations. Then it adds new features to support desirable use cases.

The RelFS proposal defines:

* The concept of immutable, hash-addressed files
* The basic operations supported by file repositories
* How to define schemas to represent metadata
* How metadata values are serialized to / deserialized from bytes
* Sketches of practical metadata and practical queries

The RelFS proposal does not cover:

* The meaning of metadata types and values
* What application should read/write what metadata
* Repository storage formats and low-level details like file packing, fragmentation, delta encoding, indexes, etc.
* Multi-user concerns such as file permissions, storage quotas, etc.
* Administrative details such as replication, fault handling, etc.


## Background and motivation

The RelFS proposal was born out of Nayuki's frustration with trying to organize personal files into hierarchies.
The most general way to store information is the hierarchy of directories and files, and this mechanism is what every major operating system provides.
However, this ubiquitous hierarchical file model is full of undesirable features:

* Contrast with hierarchical file systems
* Names suck, paths suck, length limitations, no structure (e.g. integer, fields)
* General metadata formats are brittle
* Brittle references
* Dependent metadata
* Poor unions
* Poor deduplication
* Poor sharing
* Poor propietary media libraries
* Different metadata per file format
* Nayuki's first article on this topic published in Mar 2017: [Designing better file organization around tags, not hierarchies](https://www.nayuki.io/page/designing-better-file-organization-around-tags-not-hierarchies)
* Inspiration from Git version control, Danbooru image board, BitTorrent file sharing, eDonkey2000 hash links, IPFS, Perkeep (formerly Camlistore), relational database model


## RelFS main concepts

* Files are plain blobs
* Files have no inherent name
* Files are immutable
* Files are addressed by hash
* Metadata can reference nonexistent files
* Metadata can have metadata
* Everything is a file
* Location is independent of queries


## Notes about RelFS

* Repositories are mutable
* Versioning has many possible incarnations
* File system implementation can store more copies
* Can implement stuff like file permissions, even hierarchies
* Interfaces poorly with path-based systems, but also these systems don't take advantage of hash features


## License

Copyright © Project Nayuki - https://www.nayuki.io/

Licensed as Creative Commons Attribution-ShareAlike 4.0 [(CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
