
```
FFFFFFFFFFFFFFFFFFF lllll                                              
F:::::::::::::::::F l:::l                                              
F:::::::::::::::::F l:::l                                              
FF:::FFFFFFFFF::::F l:::l                                              
  F::F       FFFFFF  l::l    æææææææææææ    ææææææææ       gggggg  gggg
  F::F               l::l    æ::::::::::æ  æ::::::::æ     g::::::gg:::g
  F:::FFFFFFFFFF     l::l    ææææææææ:::::æ:::ææææ:::ææ  g::::::::::::g
  F::::::::::::F     l::l            æ:::æ:::æ    æ:::æ g::::gggg::::gg
  F::::::::::::F     l::l     æææææææ::::æ::::ææææ::::æ g:::g    g:::g 
  F:::FFFFFFFFFF     l::l    æ:::::::::::æ:::::::::::æ  g:::g    g:::g 
  F::F               l::l   æ:::ææææ:::::æ:::ææææææææ   g:::g    g:::g 
  F::F               l::l  æ:::æ    æ::::æ::::æ         g::::g   g:::g 
FF::::FF            l::::l æ:::æ    æ::::æ:::::æ        g:::::gggg:::g 
F:::::FF            l::::l æ::::ææææ:::::æ::::::æææææ    g:::::::::::g 
F:::::FF            l::::l  æ::::::::::æ   æ::::::::æ     g::::::::::g 
FFFFFFFF            llllll   ææææææææææ     æææææææææ      gggggg::::g 
                                                                 g:::g 
                                                        gggg     g:::g 
                                                        g:::gg  gg:::g 
                                                         g::::gg:::::g 
                                                          g:::::::::g  
                                                           gg:::::gg   
                                                             ggggg   
```
[![Coverage](http://gocover.io/_badge/github.com/containous/flaeg?0)](https://gocover.io/github.com/containous/flaeg)

`Flaeg` is a Go library for dynamically building a powerful modern command line interface and loading a program configuration structure from arguments.
Go developers don't need to worry about keeping flags, command and CLI updated anymore : it works by itself !
## Overview
Do you know how boring it is to keep your CLI up-to-date ?  You will be glad to use Flaeg ;-)
This package uses your own configuration structure to build your CLI. 
You only need to describe every `StructField` with a `StructTag`,  flaeg will automatically build the CLI, parse data from args, and load Go values into Configuration structure via reflection !
## Features
 - Load your Configuration structure with program args
 - Keep your Configuration structure values unchanged if no flags called (support defaults values)
 - Many `Type` of `StructField` can be flagged :
	- type bool
	- type int (int32, int64, uint, uint64)
	- type string
	- type float (float64)
	- type time.Duration
    - type time.Time
 - Many `Kind` of `StructField` in the Configuration structure are supported :
	 - Sub-Structure
	 - Anonymous field (on Sub-Structure)
	 - Pointers on anything
 - You can add your "Parsers" on your own type like :
	 - Arrays, Slices or Maps 
	 - Your structures
 - Pointers flags are Boolean :
	 - You can give  a structure of default values for those pointers
	 - Pointer fields will get default values if their flag is called
 - Flags names are fields names by default but they can be overwritten in `StructTag`
 - "Shorthand" flags (1 character) can be added in `StructTag` as well
 - You only need to provide the root-Command which contains the configuration Structure (can be initialized), the default pointers Structure and the function to run  
 - You can add Sub-Commands to the root-Command

## Installation
To install `Flaeg`, simply run:
```
$ go get github.com/containous/flaeg
```
## Getting Started
TODO: Write usage instructions
## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D
## License
TODO: Write license
