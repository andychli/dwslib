DWSlib
======

[![Build Status](https://travis-ci.org/dfleischhacker/dwslib.svg?branch=master)](https://travis-ci.org/dfleischhacker/dwslib)

This library contains some functionality commonly used at the
[Data and Web Science Research Group](http://dws.informatik.uni-mannheim.de), University of Mannheim.

## Usage

If you use Maven for building your project, just add

```
<dependency>
  <groupId>de.uni_mannheim.informatik.dws</groupId>
  <artifactId>dwslib</artifactId>
  <version>1.0-SNAPSHOT</version>
</dependency>
```

to your pom.xml. Remember that your project has to be configured for using the DWS Maven repository. This
is done by adding

```
<repositories>
  <repository>
    <id>lski</id>
    <url>https://breda.informatik.uni-mannheim.de/nexus/content/groups/public/</url>
  </repository>
</repositories>
```

to the respective POM.

If your are not using Maven for managing dependencies, just grab it from
[this page](https://breda.informatik.uni-mannheim.de/nexus/index.html#nexus-search;gav~de.uni_mannheim.informatik.dws~dwslib~~~)
and include it in your project's dependencies.


## Content


### Framework
* Processor: Framework using multiple parallel threads to process a list of objects. The filling of the objectsToProcess and the actual processing has to be implemented. 

### Util
* DomainUtil: Collection of often used functionalities to process URLs (e.g. get PLD, Domain, Compress based on CC)
* InputUtil: Collection of often used functionalities to read input files (e.g. get all files in a directory, get input stream for file)
* Tuple: Generic class for representing ordered pairs of data
* FileUtil: Collection of often used functionalities to handle files.
* BufferedChunkingWriter: A BufferedWriter (Using GZIPOutputStream) taking care of chunking the output in multiple files.

### Virtuoso:
* LoadURI: URI Shortener (both ways) based on prefix.cc list
* Query: Virtuoso Sparql Query Processor based on direct JDBC driver (not http sparql endpoint -> no 1mio line limit)

### Others:
* Collection: collection helper methods (sortHashMapByValue, ...)
* Counter: Counter for abitrary objects (python counter like)
* MyFileReader: utf-8 file reader line-by-line; utf-8 tab (or any other character) separated file reader
