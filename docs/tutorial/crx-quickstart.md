# The `crx-quickstart` Directory

You may not have noticed this, but something interesting happened when you first started your author instance with the command 
```
java -jar ~/aem-sdk-2022/author/aem-author-p4502.jar
```
(your filepath may vary) or by clicking on the jar file through a GUI.

The first time you ran this jar file, a new folder called `crx-quickstart` was created.

(Read the CAUTION below before doing this) You can confirm this for yourself by going to the directory containing your `aem-author-p4502.jar` file; deleting the `crx-quickstart` folder that is there; and then running the jar file again. You will see that a new `crx-quickstart` directory has been made. 

CAUTION: Deleting the `crx-quickstart` directory will delete any content you've added to your local server by uploading packages or adding content through the AEM Author interface. It will also delete logs. So, do this only if you really don't trust me that running your author jar created the crx-quickstart folder.

Anyway... `crx-quickstart` should have the following directory structure:
```
|_ app/
|_ bin/
|_ conf
eula-de_DE.html
eula-en_US.html
eula-fr_FR.html
eula-ja_JP.html
|_ launchpad
|_ logs
|_ metrics
|_ opt
readme.txt
|_ repository
|_ threaddumps
```

The various `eula.html` files and the `readme.txt` contain information about Adobe's license agreement. The more interesting material is in the subdirectories.

## `app`
`app` contains a `cq-quickstart-cloudready-[...]-standalone-quickstart.jar`. I've replaced a rather cryptic sequence of characters with `[...]`. TODO: what is this file?

## `bin` 
`bin` contains binary executable files, [as you might expect](http://www.linfo.org/bin.html).

## `conf` 
`conf` contains `quickstart.properties` and `sling.properties`. TODO: I don't actually know what these do yet

## `launchpad`
`launchpad` has the following subdirectories and files:
```
|_ conf
|_ config
|_ felix
|_ installer
|_ startup
org.apache.sling.launchpad.base.jar.[...]
sling_bootstrap.txt
```
### TODO

## `logs`
`logs` contains the following files:
```
|_ access.log
|_ audit.log
|_ auditlog.log
|_ error.log
|_ history.log
|_ queryrecorder.log
|_ request.log
|_ s7access-2022-[date].log
|_ stderr.log
|_ stdout.log
|_ upgrade.log
```

TODO: describe these logs

## `metrics`
TODO

## `opt`
`opt` is empty when it is first generated. It is presumably intended for [add-on packages](https://refspecs.linuxfoundation.org/FHS_3.0/fhs/ch03s13.html) in the tradition of Unix-like operating systems.

## `repository`
TODO

## `threaddumps`

`threaddumps` contains `.txt.gz` log files. `.gz` is a file compression format that uses a GNU zip (gzip) algorithm. On MacOS, you can unzip a `.gz` file by double-clicking on the file in Finder, or by doing `gunzip [filename]` from the command line.

The logs in `threaddumps` contain, as you might expect, thread dumps. Per Oracle's [documentation](https://docs.oracle.com/cd/E13150_01/jrockit_jvm/jrockit/geninfo/diagnos/using_threaddumps.html), 
> "A thread dump is a snapshot of the state of all threads that are part of the process. The state of each thread is presented with a so called stack trace [...] A thread dump reveals information about an application’s thread activity that can help you diagnose problems and better optimize application and JVM performance; for example, thread dumps automatically show the occurrence of a deadlock."
