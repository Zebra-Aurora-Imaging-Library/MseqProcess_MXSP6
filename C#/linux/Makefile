TARGET = MseqProcess
ARCH := $(shell uname -m)
DOTNETPLATFORM=x64
ifeq ($(ARCH), aarch64)
DOTNETPLATFORM = arm64
endif

DOTNET   = dotnet
DOTNETARGS   = -c Release /p:Platform=$(DOTNETPLATFORM) /p:DefineConstants="LINUX"
DOTNETDIR = DotNet6
.PHONY   = all clean

all: $(TARGET)

clean:
	$(DOTNET) clean $(DOTNETDIR) $(DOTNETARGS) -o .
	rm -rf ref
	rm Matrox.MatroxImagingLibrary.dll

$(TARGET) : 
	$(DOTNET) build $(DOTNETDIR) $(DOTNETARGS) -o .

