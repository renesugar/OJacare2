#	$Id: Makefile,v 1.3 2004/03/19 20:42:56 henry Exp $	

TOP= ../..
include $(TOP)/Makefile.config

MLINCDIRS = 
MODULES = utilities filesystem

CMO_OBJS = $(addsuffix .cmo, $(MODULES))
CMX_OBJS = $(addsuffix .cmx, $(MODULES))

INCLUDES = $(addprefix -I , $(MLINCDIRS))

all: byte opt
byte: $(CMO_OBJS)
opt: $(CMX_OBJS)

# R�gles g�n�rales
.SUFFIXES: .ml .mli .cmo .cmi .cmx
.mli.cmi:
	$(OCAMLC) -c $(INCLUDES) $<
.ml.cmo:
	$(OCAMLC) -c $(INCLUDES) $<
.ml.cmx:
	$(OCAMLOPT) -c $(INCLUDES) $< 
clean::
	rm -f *.cm[iox] *.[so] *~ *.annot
.PHONY: realclean
realclean::
	echo -n > .depend

# D�pendances
.PHONY: depend
depend:
	$(OCAMLDEP) $(INCLUDE) *.mli *.ml > .depend

include .depend
