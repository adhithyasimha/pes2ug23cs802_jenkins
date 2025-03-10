# Makefile for hello.cpp

# Replace YOUR_SRN with your actual SRN
TARGET = pes2ug23cs802_1

# Compiler settings
CXX = g++
CXXFLAGS = -Wall -std=c++11

all: $(TARGET)

$(TARGET): hello.cpp
	$(CXX) $(CXXFLAGS) -o $(TARGET) hello.cpp

clean:
	rm -f $(TARGET)