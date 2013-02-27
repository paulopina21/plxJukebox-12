TARGET=Textures.xbt
XBMCTEX=/media/develop/jukebox/raven-11.0/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "jpg")
IMAGES += $(shell find . -name "png")
IMAGES += $(shell find . -name "gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
	$(XBMCTEX) -input . -output $(TARGET)

$(XBMCTEX): force
	$(MAKE) -C /media/develop/jukebox/raven-11.0/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

