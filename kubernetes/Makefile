TARGET = build
DOCUMENT = kubernetes.md
PRES = kubernetes.html
REVEALJS = https://github.com/hakimel/reveal.js.git

.PHONY: build


build:
	mkdir -p $(TARGET)
	cd $(TARGET)
	if [ ! -d "$(REVEALJS)" ] ; then
    	git clone --no-fail $(REVEALJS)
	fi
	pandoc -s --mathjax -i -t revealjs $(DOCUMENT) -o $(PRES)
clean:
	rm -rf $(TARGET)

default: build
