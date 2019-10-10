OBJECTS = main.o kbd.o command.o display.o \
          insert.o search.o files.o utils.o # includes all necessary files and initialized
						# the variable OBJECTS with all the .o files
# make edit calls the following command     
edit : $(OBJECTS) # specifies all the dependencies
	cc -o edit $(OBJECTS) # calls the executable "edit" and compiles it using cc
# for each of the dependencies specifies below it specifies the header files
# each of the .o files need. The .o file will only be recompiled if the timestamp 
# of the header file is newer than the .o file.    
main.o    : defs.h
files.o   : defs.h buffer.h command.h
command.o : defs.h command.h
kbd.o     : defs.h command.h
display.o : defs.h buffer.h
insert.o  : defs.h buffer.h
search.o  : defs.h buffer.h
utils.o   : defs.h
clean     :
	rm edit $(OBJECTS)
