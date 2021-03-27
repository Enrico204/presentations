
out/slides.pdf:
	mkdir -p out
	pandoc -t beamer slides.md --slide-level 3 -V theme:metropolis -V colortheme:owl -o out/slides.pdf

out/slides.pptx:
	mkdir -p out
	pandoc slides.md --slide-level 3 -o out/slides.pptx

out/slides.html: reveal.js
	mkdir -p out
	pandoc slides.md --self-contained --slide-level 3 -V theme:moon -t revealjs -o out/slides.html

reveal.js:
	wget https://github.com/hakimel/reveal.js/archive/master.tar.gz
	tar -xzvf master.tar.gz
	mv reveal.js-master reveal.js
	rm master.tar.gz

clean:
	rm -rf out
