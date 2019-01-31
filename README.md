## **BASH Library Handler** ##
#### By: Thomas Castleman 
#### Lead Dev, Drauger OS
#### <draugeros@gmail.com>
#### https://draugeros.ml
---
This program will import libraries written in BASH (MAYBE other scripting langauges), written for BASH, and allow a programmer to use them in any program.

Most of this will be written in BASH for simplicity's sake, but do not expect all of it to be like that. There very well may be parts in Python, C++, C, or some other language if functionality requires it.

#   USAGE
first, a programmer will be able to pass 2 values to import:
#   library path and name
Pass the library name along with the path to it, if it is not in the same directory that import will end up working. It is advised to pass the path, to ensure it works properly

#   module name
modules will be denoted using specific names, which will allow them to be isolated and passed back to the calling function
This means usage will be defined as:

   `var=$(import /path/to/library/foo foobar)`

Wheras running modules from these libraries will be done as:

   `input="data to be passed"`
   
   `eval $var`

Where $input is some variable containing the necissary data for the module to work.
Modules will set their output (if there is any) to the OUTPUT variable, followed by the order it was generated (OUTPUT0 first, OUTPUT1 second, etc)

##NOTE
   If no module name is passed to import, it will be assumed that the user wants the entire library passed. At which point, it will be. 
   It then falls to the user to parse these libraries
