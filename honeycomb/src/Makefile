BUILD_DIR=../build
LATEX_OPTS=--output-directory=$(BUILD_DIR)
OBJ=$(BUILD_DIR)/honeycomb.pdf

all: $(BUILD_DIR) $(OBJ)

$(BUILD_DIR):
	mkdir -p $@

$(BUILD_DIR)/%.pdf: %.tex
	pdflatex $(LATEX_OPTS) -shell-escape "$<"

objclean:
	rm -rf $(BUILD_DIR)

bkpclean:
	rm -f *~

clean: objclean

dstclean: objclean bkpclean

#  Local Variables:
#    coding:utf-8
#    mode:Makefile
#  End:
