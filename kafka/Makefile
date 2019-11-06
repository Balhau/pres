TARGET = build
DOCUMENT = kafka.md
PRES = kafka.html
REVEAL_PATH=reveal.js
REVEALJS = https://github.com/hakimel/$(REVEAL_PATH).git

.PHONY: build


build:
	mkdir -p $(TARGET); \
	cp -r img $(TARGET); \
	cd $(TARGET); \
	[ ! -d "$(REVEAL_PATH)" ] && git clone $(REVEALJS); cd ..; \
	pandoc --slide-level=2 -s --mathjax -i -t revealjs $(DOCUMENT) -o $(TARGET)/$(PRES)
clean:
	rm -rf $(TARGET)

default: build
