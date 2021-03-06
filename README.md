O'Jacare 2
An object-oriented interface between O'Caml and Java
------------------------------------------------------------------------------
$Date: 2014/07/18 09:32:16 $


------------------------------------------------------------------------------
Principle
------------------------------------------------------------------------------
O'Jacare 2 is a code generator to help in interoperability between Java and 
O'Caml through their object model. O'Jacare defines a simple IDL for Java's 
classes and interfaces descriptions. For communications from Java to O'Caml 
it owns a callback mechanism. So, you can override in O'Caml a method 
defined in Java or implement a Java interface in O'Caml. 
The implementation uses the OCaml-Java compiler.
O'Jacare generates all needed wrapper classes and enables static 
typechecking in both world.

* Web-site:
    http://www.github.com/beaCarre/OJacare2

* OCaml-Java:
    http://www.ocamljava.org/

* O'Caml: 
    http://caml.inria.fr/

* Java:   
    http://java.sun.com/


------------------------------------------------------------------------------
Installation
------------------------------------------------------------------------------
See INSTALL


------------------------------------------------------------------------------
Usage
------------------------------------------------------------------------------
O'Jacar�'s IDL have a syntax similar to Java syntax.
The command line tool 'ojacare' take an idl file in argument.
It generate an Caml module (named as the idl file), 
and some Java classes in a package named callback.
This generated code, depends on the 'ocamljava' compiler,
but users could now see a Java object as a Caml object.
The callback mechanism allow to subclass in Caml a class implemented in Java.


------------------------------------------------------------------------------
Examples
------------------------------------------------------------------------------
See the directory examples/

------------------------------------------------------------------------------
Documentation
------------------------------------------------------------------------------
See website : http://www.pps.jussieu.fr/~henry/ojacare/documentation.en.html

See directory Rapport/ for further informations.

-------------------------------------------------------------------------------
Licence: 
-------------------------------------------------------------------------------
See file LICENSE

-------------------------------------------------------------------------------
Contacts:
-------------------------------------------------------------------------------
Beatrice.Carre@etu.upmc.fr

Emmanuel.Chailloux@lip6.fr

xclerc@ocamljava.org

Gregoire.Henry@ocamlpro.com

$Id: README,v 1.6 2014/07/18 09:32:16 beatrice Exp $
