#!/usr/bin/make -f

PROJECT = gdrive-indicator

GETTEXT = /usr/bin/xgettext
MSGMERGE = /usr/bin/msgmerge

PO = $(shell find . -name '*.po' -print | sed -e 's!./!!g')

update-po:
	$(GETTEXT) -f POT_PY_FILES -L python -d $(PROJECT) -o $(PROJECT).pot
	for lang in $(PO); do $(MSGMERGE) -U $$lang $(PROJECT).pot; done
