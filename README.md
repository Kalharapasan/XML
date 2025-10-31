What is XML?

XML stands for eXtensible Markup Language, a markup language similar to HTML. It is
designed to store and transport data. XML became a W3C Recommendation in February 1998.

While HTML is designed to display data (focusing on how data looks), XML is designed to
carry data (focusing on what the data represents). XML does not have predefined tags like
HTML. XML stores data in plain text, which provides a software- and hardware-independent
way of storing, transporting, and sharing data. This makes it easier to move data between
systems, applications, browsers, and platforms without losing information.

XML naming rules:

- Element names are case-sensitive.
- Element names must start with a letter or an underscore (_).
- Element names cannot start with the letters "xml" in any combination of upper/lower case (for example: xml, XML, Xml).
- Element names can contain letters, digits, hyphens (-), underscores (_), and periods (.).
- Element names cannot contain spaces.

## Syntax of XML (rules)

Here are the most important syntax rules you should follow when writing XML documents.

- Every XML document must have a single root element that contains all other elements.

Example:

```xml
<root>
    <child>value</child>
</root>
```

- XML documents can start with an optional XML prolog (recommended):

```xml
<?xml version="1.0" encoding="UTF-8"?>
```

- All elements must have a closing tag (or be self-closing):

Correct:

```xml
<title>Harry Potter</title>
```

Self-closing:

```xml
<br />
```

- XML tags are case-sensitive. The opening and closing tag names must match exactly.

Correct:

```xml
<title>Harry Potter</title>
```

Incorrect (mismatched case):

```xml
<title>Harry Potter</Title> <!-- not allowed -->
```

- Elements must be properly nested.

Incorrect:

```xml
<b><i>This text is bold and italic</b></i> <!-- not allowed -->
```

Correct:

```xml
<b><i>This text is bold and italic</i></b>
```

- Attribute values must always be quoted (single or double quotes):

```xml
<note date="2007-12-11">Remember this date</note>
```

- Use predefined entity references to represent special characters inside element content or attribute values:

- &amp;lt;  →  &lt;  (less-than)
- &amp;gt;  →  &gt;  (greater-than)
- &amp;amp; →  &amp;  (ampersand)
- &amp;apos; →  '  (apostrophe)
- &amp;quot; →  "  (quotation mark)

These rules form the basis of well-formed XML. To be valid XML, a document must be well-formed and also conform to any schema (DTD, XSD) it declares.
