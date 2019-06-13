# Go Utilities [![Build Status](https://travis-ci.com/CameronSchafer/go-utils.svg?branch=master)](https://travis-ci.com/CameronSchafer/go-utils)
-------

_Go Code formatter, linter, tester and runner all in one_

## Script Setup
-------
### Mac:
1. Make sure the script is executable by running: __chmod 775 go-utils__
2. If needed create an alias for the script so it can be easily called from anywhere by adding an alias entry in the .bash_profile file.
> This file is located in the HOME directory. Use any text editor and add the line: __alias your-alias="path-to-script"'__ where "path to script" is the location of the go-utils script and your-alias is the alias that you choose. e.g. if the script is in the HOME directory then the addition would be: _alias gou="~/./go-utils"_
  
## Usage
-------
* This script needs to be run from within the same folder of main.go.  
* Currently can only see files within the same folder.  

If an alias was created for this script then use that alias within the go folder that you want to test. Otherwise call the bash script as a normal bash script, using _./path-to/go-utils_  
For running the all in one (gofmt, golintci, test and run main.go): 
```
 ./path-to/go-utils
```  
Run only main.go: `./path-to/go-utils -r`  
Test only: `./path-to/go-utils -t`  
Verbose test: `./path-to/go-utils -vt`  
Lint only: `./path-to/go-utils -l`  
Verbose lint: `./path-to/go-utils -vl`  

To change to light mode: `./path-to/go-utils -m light`

### Usage Help:
./path-to/go-utils [-m <light|dark>] [-v] [-l] [-t] [-r]  
> -m  mode light|dark  [ default is dark ]. If running go-utils in a terminal with a dark background, either mode is fine. If running in a white or light background, then use the light mode to make the colours more readable.   

> Only one of the following args can be run at a time.  
> The first arg in the command [ ./path-to/go-utils -rlt ] will only use [-r] before exiting.  
-l  lint files only mode    [ -vl  for verbose linting ]  
-t  test program only mode  [ -vt  for verbose testing ]  
-r  run program only mode  
-v  run command in verbose mode  

To note here, 
* verbose mode will only run if verbose is called before the main argument.
* lighting mode will only have an effect when running everything together.
