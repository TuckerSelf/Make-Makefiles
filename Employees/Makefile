#/**
# * @file Makefile
# * @author Tucker Self
# * @date 2023-09-21
# * @brief the makefile for the employees file system
# * 
# * allows for the usage of make commands for the code within the employees file
# */

CC = g++
CFLAGS = -g -Wall -Wextra
TARGET = employees

all: $(TARGET)

$(TARGET): $(TARGET).c
	$(CC) $(CFLAGS) -o $(TARGET) $(TARGET).c

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) -c Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) -c Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) -c Supervisor.cpp

main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) -c main.cpp

clean:
	$(RM) $(TARGET) *.o *~
