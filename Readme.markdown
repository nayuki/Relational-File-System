Relational File System, ongoing development version
===================================================


## Introduction

The Relational File System (RelFS):

* Addresses the limitations of hierarchies
* Defines a model of immutable, hash-addressed files
* Defines a meta-schema for metadata files and a standard serialization
* Does not define a storage format or rich features
* Does not define administrative features or query formats


## Motivation

* Contrast with hierarchical file systems
* Names suck, paths suck
* Brittle references
* Dependent metadata
* Poor unions
* Poor deduplication
* Poor sharing
* Poor propietary media libraries
* Different metadata per file format


## Core tenets

* Files are plain blobs
* Files have no inherent name
* Files are immutable
* Files are addressed by hash
* Metadata can reference nonexistent files
* Metadata can have metadata
* Everything is a file
* Location is independent of queries


## Background info

* Plight of Nayuki trying to organize personal files
* Nayuki's first article on this topic published in Mar 2017: [Designing better file organization around tags, not hierarchies](https://www.nayuki.io/page/designing-better-file-organization-around-tags-not-hierarchies)
* Inspiration from Git version control, Danbooru image board, BitTorrent file sharing, eDonkey2000 hash links, IPFS, Perkeep (formerly Camlistore), relational database model


## Notes

* Repositories are mutable
* Versioning has many possible incarnations
* File system implementation can store more copies
* Can implement stuff like file permissions, even hierarchies
* Interfaces poorly with path-based systems, but also these systems don't take advantage of hash features


## License

Copyright © Project Nayuki - https://www.nayuki.io/

Licensed as Creative Commons Attribution-ShareAlike 4.0 [(CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
