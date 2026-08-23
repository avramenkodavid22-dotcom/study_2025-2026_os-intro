# Makefile для компиляции отчета
FILE_NAME = report
OUTPUT_DIR = _output

all: pdf docx

pdf:
	mkdir -p $(OUTPUT_DIR)
	pandoc $(FILE_NAME).md -o $(OUTPUT_DIR)/$(FILE_NAME).pdf \
		--pdf-engine=xelatex \
		--standalone \
		--self-contained \
		--number-sections \
		--toc \
		--toc-depth=2 \
		--metadata lang=ru-RU

docx:
	mkdir -p $(OUTPUT_DIR)
	pandoc $(FILE_NAME).md -o $(OUTPUT_DIR)/$(FILE_NAME).docx \
		--standalone \
		--self-contained \
		--number-sections \
		--toc \
		--toc-depth=2 \
		--metadata lang=ru-RU

clean:
	rm -rf $(OUTPUT_DIR)

help:
	@echo "Доступные команды:"
	@echo "  make pdf  - создать PDF"
	@echo "  make docx - создать DOCX"
	@echo "  make all  - создать PDF и DOCX"
	@echo "  make clean - удалить папку _output"
