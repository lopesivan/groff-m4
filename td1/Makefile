NAME     = TD1

M4       = $(NAME).m4
MS       = $(NAME).ms
MAIN     = $(NAME).tex
PDF      = $(NAME).pdf

all: $(PDF)

$(MS): $(M4)
	m4 -I$PWD gpic.m4 $^ > $@

$(PDF): $(MS)
	groff -ms -U -e -p -KUTF-8 -Tdvi $^ | dvipdfm > $@

clean:
	rm -f $(PDF) $(MS)

show: $(PDF)
	zathura $(PDF)

