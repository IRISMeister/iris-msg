# iris-msg

## To build
```
# ./build.sh
```

## To run
```
# ./up.sh
```

```
$ docker compose exec iris iris session iris "local1"
現在のプロセスの言語: ja
(現在のロケールの)デフォルトの言語: ja
おはよう
おはよう
おはよう 2
おはよう 2
こんにちは
こんばんは
$ docker compose exec iris iris session iris "load"
$ docker compose exec iris iris session iris "local1"
現在のプロセスの言語: ja
(現在のロケールの)デフォルトの言語: ja
おはよう
Good morning
おはよう 2
おはよう 2
こんにちは
こんばんは

$ docker compose exec iris iris session iris -U%SYS '##class(Config.NLS.Locales).Install("enuw")'
$ docker compose exec iris iris session iris "local1"
現在のプロセスの言語: en
(現在のロケールの)デフォルトの言語: en
Good morning
Good morning
Good morning 2
Good morning 2
Hello
Good evening
$ docker compose exec iris iris session iris "##class(Local).test1()"
Good morning
```

## To completely remove (including databases)
```
# ./down.sh
```

