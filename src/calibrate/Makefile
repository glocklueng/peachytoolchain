UIC = pyside-uic
UIC_OPT = -x

RCC = pyside-rcc
RCC_OPT =

.PHONY: clean

UI_FILES = $(wildcard *.ui)
#RESOURCE_FILES = $(shell find ../resources -name *.qrc)

%.py: %.ui
	$(UIC) $(UIC_OPT) -o $@ $<

#%_rc.py: %.qrc
#    $(RCC) $(RCC_OPT) -o $@ $<
#    -cp $@ ./

ui: $(UI_FILES:.ui=.py)

clean:
	rm -f $(UI_FILES:.ui=.py)
