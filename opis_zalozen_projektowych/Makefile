PAPER=main.tex

all:
	rubber --pdf $(PAPER)

show:
	zathura $(PAPER:.tex=).pdf &>/dev/null

watch:
	@while [ true ]; do inotifywait -e MOVE_SELF $(PAPER); sleep 1; make all; done

clean:
	rubber --clean $(PAPER)
