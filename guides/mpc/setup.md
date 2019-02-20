MPC Setup Instructions
=========================

This document gives instructions on how to setup the 
[Makefile Project Workspace Creator](https://github.com/DOCGroup/MPC) build 
tool for your development environment. 

Installation
-------------

Download [MPC](https://github.com/DOCGroup/MPC) from its Github repo, and place
it in a easy to locate directory.

> We recommend you do not place the project in a directory that contains spaces. We
> also recommend you put the project in a short directory (_e.g._, `/proj/MPC`).

Next, set the `MPC_ROOT` environment variable to the location where you placed
the MPC project. This will allow us to access the `MPC_ROOT` environment variable
when we define other environment variable and use the command line. Using `/proj/MPC` 
as an example:

### Linux/Unix-based Systems

    export MPC_ROOT=/proj/MPC
    
### Windows-based Systems

    set MPC_ROOT=/proj/MPC

Lastly, we need to add `MPC_ROOT` to your `PATH` environment variable. This will
allow us to run the `mwc.pl` command from any directory when using the command-line.

### Linux/Unix-based Systems

    export PATH=$PATH:$MPC_ROOT
    
### Windows-based Systems

    set PATH=%PATH%;%MPC_ROOT%
    
Running MPC
-------------    

If we setup our environment correctly, we can now run `mwc.pl` from any directory
when using the command-line.

    mwc.pl -type vc12
    
This will generate a Visual Studio workspace by recursively pulling in any project it
finds in the subdirectories.

> If you are using Windows, you must install a PERL executable such as 
> [ActivePERL](https://www.activestate.com/products/activeperl/) to run the `mwc.pl` PERL 
> script.   
