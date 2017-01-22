AM_CFLAGS=$(GLIB_CFLAGS)
AM_CFLAGS+=$(SQLITE3_CFLAGS)

bin_PROGRAMS=duperemove hashstats btrfs-extent-same csum-test show-shared-extents
man8_MANS=duperemove.8 hashstats.8 btrfs-extent-same.8 show-shared-extents.8

duperemove_SOURCES=duperemove.c debug.c csum.c file_scan.c run_dedupe.c dedupe.c filerec.c results-tree.c hash-tree.c util.c dbfile.c memstats.c find_dupes.c csum-murmur3.c btrfs-util.c csum-xxhash.c rbtree.c interval_tree.c list_sort.c xxhash.c
duperemove_LDADD=$(GLIB_LIBS)
duperemove_LDADD+=$(SQLITE3_LIBS)

hashstats_SOURCES=hashstats.c filerec.c rbtree.c util.c debug.c csum.c dbfile.c csum-murmur3.c hash-tree.c csum-xxhash.c xxhash.c list_sort.c
hashstats_LDADD=$(GLIB_LIBS)
hashstats_LDADD+=$(SQLITE3_LIBS)

csum_test_SOURCES=csum-test.c csum.c csum-murmur3.c csum-xxhash.c xxhash.c util.c debug.c

show_shared_extents_SOURCES=filerec.c debug.c util.c rbtree.c
show_shared_extents_LDADD=$(GLIB_LIBS)
show_shared_extents_CPPFLAGS=-DFILEREC_TEST
