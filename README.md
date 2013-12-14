shared-memory-size
==================

http://d.hatena.ne.jp/naoya/20080212/1202830671
のshared_memory_size.plをFatPackerを使って1ファイル化しました

1ファイル化
-----------

```
$ cpanm install App::FatPacker
$ cpanm Linux::Smaps
$ fatpack pack shared-memory-size.pl >shared_memory_size_1file.pl
$ chmod 755 shared_memory_size_1file.pl
```


実行方法
--------

```
$ sudo ./shared_memory_size_1file.pl `pgrep apache2`
PID	RSS	SHARED
8214	12296	10704 (87%)
19940	15236	8728 (57%)
19941	14640	8516 (58%)
19942	14256	8444 (59%)
19943	14248	8588 (60%)
19944	14804	8484 (57%)
21291	14460	8476 (58%)
22644	14360	8648 (60%)
22645	8028	7808 (97%)
22646	15168	8584 (56%)
22647	8024	7804 (97%)
```

