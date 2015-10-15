# SENG301-PlantUML-Config
### PlantUML config file for SENG301 UML specification.
_This file is of course unofficial and thus any syntactical errors caused by its use are the fault of the user, and the user alone._

This config file is intended to simplify the look of Class/Sequence/State
diagrams to meet the standard set for SENG301.
It uses monochrome by default, but this can be overriden if needed.

Due to missing formatting options, the user should use Class syntax for
Object diagrams, in order to get the desired look.

### Usage:

As with any config file, add it to your preprocessor directives with:
```
!include SENG301.config
```
_NOTE: This assumes the config file is in your working directory, 
if it's not you need to provide the path._

You can specify the use of this file in the command line with the -config
argument as well.

#### Class Diagrams:

PlantUML works nearly perfectly for Class diagrams, with the exception of
access levels on classes, if you want to specify that declare the class
as such:
```
Class className as "$ClassName"
```
where $ is the desired access level. 

#### Sequence Diagrams:

Sequence diagrams work basically perfectly, 
just make sure you activate/deactivate your objects on the correct lines.

#### Object Diagrams:

It is recommended that you use Class diagrams for Object diagrams as well,
because Objects cannot be given aliases and : can't be used in names. 
Keep in mind that double underscores are used to denote underlines.

#### State Diagrams:
To use State diagrams add:
```
hide empty description
```
to you file, however you need to add line breaks in your
arrow descriptions using '\n' to ensure that the descriptions do not
become too long.

_There are a few other minor Syntactical quirks, but most can be easily 
worked around._
