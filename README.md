# **PEC**

![license](https://img.shields.io/github/license/phrenotype/pec)
![contributors](https://img.shields.io/github/contributors/phrenotype/pec)
![contributors](https://img.shields.io/github/languages/code-size/phrenotype/pec)

```shell
>> pec 5
16023976762414081
```
This is a unique id (64-bit integer) generator that can be used to generate unique identifiers for objects and database fields.

It currently supports linux and macOs, and work is in progress to add support for windows.

## Why Use Pec ?

1. To maintain sanity in your distributed system.
2. If you do not wish to use auto-incremented primary keys.
3. To avoid issues when you shard your SQL databases.
4. If you constantly move data and you would like your fields / objects to remain unique.


## Install

`composer require pec/pec`

# Bit Distribution
TIMESTAMP ---------- 45 BITS

CUSTOM BITS -------  9 BITS

SEQUENCE BITS -----  10 BITS

## Usage
Copy the file `pec` and add it to your PATH, or you can refer to it using it's absolute path.

The default epoch is January 1st, 2022.

The only thing you need to pass is a customId. It could be any number between 0 and 511 (both inclusive).

Please once you use a customId to generate id's for a project, you must keep using that customId for that project.

Using a customId of `5`
```shell
>> pec 5
16023976762414081
```

To use your own timestamp,

```shell
>> pec 5 1652991600000
16023976762414081
```

Now, to use it from a script, you can use the `system` or `exec` commands or whatever function your framework or language offers to run shell commands.

For instance in php,

```php
<?php

$id = system("pec 5")

echo $id;
```

## OS support
For now, only linux and macOS are supported. Support for windows will soon be added.


## Contribution
To contribute, contact the email below.

## Contact
**Twitter** : [@phrenotyper](https://twitter.com/phrenotyper)

**Email** : paul.contrib@gmail.com

