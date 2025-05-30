# python-docx

*python-docx* is a Python library for reading, creating, and updating Microsoft Word 2007+ (.docx) files.

This specific fork attempts to catch up with some feature-addition pull requests from the community, and 
test them as is feasible both with existing unit tests, and through its use in an internal project
that makes extensive use of python-docx. We also run compatibility tests from python 3.9 onwards, and the
test suite on python 3.8+, at least on macOS/Darwin.

## Installation

```
pip install python-docx
```

## Example

```python
>>> from docx import Document

>>> document = Document()
>>> document.add_paragraph("It was a dark and stormy night.")
<docx.text.paragraph.Paragraph object at 0x10f19e760>
>>> document.save("dark-and-stormy.docx")

>>> document = Document("dark-and-stormy.docx")
>>> document.paragraphs[0].text
'It was a dark and stormy night.'
```

More information is available in the [python-docx documentation](https://python-docx.readthedocs.org/en/latest/)
