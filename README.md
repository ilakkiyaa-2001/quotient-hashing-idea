# quotient-hashing-idea
A novel approach for hash index calculation using quotient rehashing.

# Quotient Hashing Idea

## Overview
This repository explores a novel approach to hash index calculation by rehashing the quotient of the hash value. This method could potentially improve hash distribution and reduce clustering in hash tables.

## Key Idea
1. Compute the hash value of the key: `h = Hash(key)`.
2. Calculate the quotient: `q = h // table_size`.
3. Rehash the quotient to compute the index: `index = q % table_size`.

## Example Code
Here's a simple Python implementation:

```python
def hash_index(key, table_size):
    initial_hash = hash(key)
    quotient = initial_hash // table_size
    return quotient % table_size

