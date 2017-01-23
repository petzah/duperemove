AM_CFLAGS=$(GLIB_CFLAGS)
AM_CFLAGS+=$(SQLITE3_CFLAGS)

if DEBUG
AM_CFLAGS+=-ggdb3 -fsanitize=address -fno-omit-frame-pointer
AM_CPPFLAGS=-DDEBUG_BUILD
endif

bin_PROGRAMS=duperemove hashstats btrfs-extent-same csum-test show-shared-extents
man8_MANS=duperemove.8 hashstats.8 btrfs-extent-same.8 show-shared-extents.8

duperemove_SOURCES=duperemove.c csum.c csum.h filerec.c filerec.h hash-tree.c hash-tree.h results-tree.c results-tree.h dedupe.c dedupe.h util.c util.h btrfs-util.c btrfs-util.h dbfile.c dbfile.h stats.h memstats.c memstats.h debug.c debug.h file_scan.c file_scan.h find_dupes.c find_dupes.h run_dedupe.c run_dedupe.h interval_tree.c interval_tree.h rbtree.c rbtree.h csum-murmur3.c list_sort.c list_sort.h xxhash.c xxhash.h csum-xxhash.c list.h kernel.h btrfs-ioctl.h interval_tree_generic.h rbtree_augmented.h
duperemove_LDADD=$(GLIB_LIBS)
duperemove_LDADD+=$(SQLITE3_LIBS)

hashstats_SOURCES=hashstats.c filerec.c filerec.h debug.c debug.h util.c util.h csum.c csum.h csum-murmur3.c csum-xxhash.c rbtree.c rbtree.h hash-tree.c hash-tree.h dbfile.c dbfile.h list_sort.c list_sort.h memstats.h xxhash.c xxhash.h file_scan.h rbtree_augmented.h kernel.h list.h interval_tree.h bswap.h
hashstats_LDADD=$(GLIB_LIBS)
hashstats_LDADD+=$(SQLITE3_LIBS)

csum_test_SOURCES=csum-test.c csum.c csum.h csum-murmur3.c csum-xxhash.c util.c util.h xxhash.c xxhash.h debug.c debug.h

show_shared_extents_SOURCES=filerec.c filerec.h debug.c debug.h rbtree.c rbtree.h util.c util.h memstats.h interval_tree.h kernel.h list.h rbtree_augmented.h
show_shared_extents_LDADD=$(GLIB_LIBS)
show_shared_extents_CPPFLAGS=-DFILEREC_TEST

EXTRA_DIST=$(man8_MANS)
EXTRA_DIST+=docs README.md LICENSE.xxhash LICENSE SubmittingPatches rbtree.txt README.autotools
EXTRA_DIST+=stats.c csum-sha256.c  # include code which is not being compiled
