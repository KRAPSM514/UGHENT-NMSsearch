
# NMS Search
A tool for fast similarity search of genomic sequences, using [NMSLIB](https://github.com/nmslib/nmslib).

This code is developed by a research team of Ghent University Global Campus.


## How to Use
NMSSearch supports two algorithms to index sequences, using vantage-point search trees and using hierarchical navigable small world graphs. Generally, HNSW takes much longer to build the index, but is faster at query time.

To build an index for a FASTA file of target sequences:
```javascript
nmssearch --algorithm hnsw build <my-fasta-file.fa>

```
To query the index, given a FASTA of sequences to look up:
```javascript
nmssearch --algorithm hnsw query hnsw <my-queries.fa>
```
The name of the generated index is currently hardcoded as hnsw or vptree.

