TARGET	= MseqProcess
CFLAGS   = -I$(MILDIR)/include -g -Werror
CXXFLAGS = $(CFLAGS) -std=c++11
LDFLAGS  = -L$(MILDIR)/lib -lmil
.PHONY   = all clean

all: $(TARGET)

clean:
	-rm -f $(TARGET) $(TARGET).o

$(TARGET) : $(TARGET).o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDFLAGS) 
