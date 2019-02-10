JC		= javac
JFLAGS		= -g

ENTRY_CLASS	= Main

SRC_DIR		= src
CLASS_DIR	= bin
SRC_FILE	= $(SRC_DIR)/*.java
MANIFEST_FILE	= $(CLASS_DIR)/MANIFEST.MF
JAR_FILE	= $(notdir $(shell pwd)).jar

.PHONY: all
all: $(CLASS_DIR) $(MANIFEST_FILE) $(JAR_FILE)
$(CLASS_DIR):
	mkdir -p $@

$(MANIFEST_FILE):
	echo "Main-Class: $(ENTRY_CLASS)" > $(MANIFEST_FILE)

$(JAR_FILE): $(SRC_FILE)
	$(JC) $^ -d $(CLASS_DIR) $(JFLAGS)
	jar -cvfm $@ $(MANIFEST_FILE) -C $(CLASS_DIR) .


.PHONY: clean
clean:
	rm -rf $(CLASS_DIR)  $(JAR_FILE) 


.PHONY: run
run:
	@java -jar $(JAR_FILE)
