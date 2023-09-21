#/**
# * @file Makefile
# * @author Tucker Self
# * @date 2023-09-21
# * @brief the makefile for the employees file system
# * 
# * allows for the usage of make commands for the code within the employees file
# */

#Compile using g++
CC = g++
#Compile with all errors and warnings
CFLAGS = -g -Wall -Wextra
#The build target
TARGET = employees

#Compilation commands
all: $(TARGET)

$(TARGET): Employee.o Officer.o Supervisor.o main.o
	$(CC) $(CFLAGS) -o $(TARGET) Employee.o Officer.o Supervisor.o main.o

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) -c Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) -c Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) -c Supervisor.cpp

main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) -c main.cpp

#Clean up files
clean:
	$(RM) $(TARGET) *.o *~
