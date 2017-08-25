# KiCad Python - Style Guide and Development Resources
## Status of this document
24 Aug 2017 - This document is submitted to the developer's mailing list for discussion.

## Development Resources
- [Python Plugin Development for Pcbnew](http://docs.kicad-pcb.org/doxygen/md_Documentation_development_pcbnew-plugins.html)
- [Python Scripting Reference](http://docs.kicad-pcb.org/stable/en/pcbnew.html#_kicad_scripting_reference)
- [pcbnew Python API](http://docs.kicad-pcb.org/doxygen-python/namespacepcbnew.html)
- [KiCad Developer - General Information](http://kicad-pcb.org/contribute/developers)
  - KiCad C++ Source Code Style Guide: [Doxygen/HTML](http://docs.kicad-pcb.org/doxygen/md_Documentation_development_coding-style-policy.html); [pdf](https://lists.launchpad.net/kicad-developers/pdfmQbEHNFKLc.pdf)
  - [User Interface Guidelines](http://docs.kicad-pcb.org/doxygen/md_Documentation_development_ui-policy.html)  
- [KiCad Source](https://github.com/KiCad/kicad-source-mirror)
  - [KiCad Source - Master](https://github.com/KiCad/kicad-source-mirror/tree/master)
  - [KiCad Source - 4.0](https://github.com/KiCad/kicad-source-mirror/tree/4.0)
- [PEP8](https://www.python.org/dev/peps/pep-0008/)
  - [Beyond PEP8](https://www.youtube.com/watch?v=wf-BqAjZb8M) (video, 52 minutes)

## Brief Guide to KiCad PEP8

Your code should follow PEP8 with the exception of the KiCad 
variations noted below.

### KiCad variations from PEP8

Our C++ coding policy, and therefore our Python policy, is 100 characters.
Function names are CamelCase or mixedCase.

### KiCad Naming Conventions
      ClassName
      functionName *or* FunctionName (PEP8 primarily recommends 'function_name')
      function_parameter
      parameter_disambiguation_ (from standard keywords)
      variable_name
      _nonpublic_function
      _nonpublic_global_variable
      CONSTANT_VALUE_NAME

## *Beyond PEP8* Recommendations
- If appropriate, define **\_\_len__** and **\_\_getitem__** in your class to create a sequence
- If appropriate, define **\_\_enter__** and **\_\_exit__** in your class to allow the
use of **with** keyword.    
- Use **@property** to allow dotted notation for 'getter' functions.
- Instead of using indexes for tuples, **from Collections import namedtuple**

## Development and Distribution Logistics

- If this is an extension to KiCad, write your script as an
[Action Plugin](http://docs.kicad-pcb.org/doxygen/md_Documentation_development_pcbnew-plugins.html)
- Format and comment your code according to these guidelines.
- Make your code available on [github](github.com).
- Write a user's guide in the form of a README.md in the root folder on *github*.
- Create a thread on KiCad Forums' [Projects > External Plugins](https://forum.kicad.info/c/projects/external-plugins) category to announce, discuss, and get feedback from the user community.
- Once honed and polished, reach out to the developor community on the [developer's mailing list](https://lists.launchpad.net/kicad-developers/) for discussion and feedback.
- You must submit a patch (preferably using **git format-patch** against the
HEAD of the [KiCad master branch](https://github.com/KiCad/kicad-source-mirror/tree/master)) to the [developer's mailing list](https://lists.launchpad.net/kicad-developers/) so
developers can test and comment on it.
- Once it has been approved, it
can be merged into the master branch.  It may take some time and several
iterations to get the approval of the lead developers so please be patient.
