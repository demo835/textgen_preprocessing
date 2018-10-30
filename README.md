# Text Generation Preprocessing Module
A python module preparing text for training in a neural network. Designed specifically for processing works of fiction.

In my experience, AI text generation requires several steps preceeding and following training in a neural network in order to produce comprehensible text. This module is intended to reduce network loss and improve accuracy of generated sentence structures.

## Features
-**Dialogue Removal** - Verbal communication differs significantly from narrative language. Better outcomes are achieved by training dialogue separately from narration.

-**Newline Removal** - Newline characters (\n) can slow down training, increase character dictionaries and file size, and confuse NLP libraries such as spaCy.

## How to Use
This module requires the spaCy library. @explosion/spaCy

`pip install -U spacy`

It requires a text document containing text encoded in UTF-8. Change filename below to match your text document filename:

`text = open(u"./source-gaunt-unprepared.txt", encoding="utf8", errors='ignore').read()[start_index:end_index]`

Open a terminal and run:

`python text-prep.py`

Processed text will output to a new file called processed.txt. Upload file to be trained in a network such as https://github.com/minimaxir/textgenrnn @minimaxir
