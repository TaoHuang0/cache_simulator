I developed three different versions of
a cache simulator:

* Direct Mapped Read-Only Cache

  This version only needs to support reading bytes from an address.
  
* Fully Associative Write Through Cache

  This version supports both reading and writing bytes from an address.
  There is only one set of cache lines so the number of set index bits is known
  to be zero. The number of cache lines is specified when the cache is created.
  The replacement policy is "least recently used".

* Set Associative Write Back Cache

  This version implements a general set-associative cache with reading and writing
  with "write back". Within a set of cache lines, least recently used is the replacement
  policy. Write back means that when a byte is written, it is only written to the cache line
  without immediately updating main memory. A "dirty" cache line is written back in its entirety
  to the main memory when it is replaced. This version also supports "flushing" the cache which
  means writing back any dirty cache lines and invalidating all cache lines to reset the cache
  to empty.
