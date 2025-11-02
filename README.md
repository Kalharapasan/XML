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


Questions 01
Write an XML document containing root/parent element, attributes, child elements, sub-child elements

0. University Lecturers

1. Bank Customers

2. Hospital Patients

Find your last digit of your registration number. Get the last digit and divide by 3.

If the reminder is

0 = University Lecturers

1 = Bank Customers

2 = Hospital Patients

Example: SEU/IS/17/ICT/145, Last Digit is 5 5/3 Reminder = 2 Therefore, Topic is Hospital Patients

## Exercises — Questions 01

Write an XML document that includes a root (parent) element, attributes, child elements, and at least one sub-child element.

Available topics (choose one using the rule below):

- 0 — University Lecturers
- 1 — Bank Customers
- 2 — Hospital Patients

How to choose your topic

- Take the last digit of your registration number.
- Divide that digit by 3 and compute the remainder (modulo 3).
- Choose the topic using the remainder:
  - 0 → University Lecturers
  - 1 → Bank Customers
  - 2 → Hospital Patients

Example

Registration: SEU/IS/17/ICT/145

Last digit = 5

5 ÷ 3 = 1 remainder 2 (5 % 3 = 2)

Topic → Hospital Patients

Deliverable

- Create an XML file (for example, topic.xml) containing:
    - A root element named appropriately for the chosen topic (for example: `<University>`, `<Bank>`, or `<Hospital>`).
    - At least two attributes on the root element (for example: id, campus, branch).
    - At least two child elements with text content or further nested elements.
    - At least one sub-child element (a nested element inside a child element).

Sample XML skeletons

University Lecturers:

```xml
<University id="U001" campus="Main">
    <Lecturers>
        <Lecturer>
            <Name>Dr. Jane Doe</Name>
            <Department>Computer Science</Department>
        </Lecturer>
    </Lecturers>
</University>
```

Bank Customers:

```xml
<Bank branch="Central" id="B001">
    <Customers>
        <Customer>
            <Name>John Smith</Name>
            <Account>
                <Number>12345678</Number>
                <Type>Savings</Type>
            </Account>
        </Customer>
    </Customers>
</Bank>
```

Hospital Patients:

```xml
<Hospital id="H001" name="City Hospital">
    <Patients>
        <Patient>
            <Name>Mary Johnson</Name>
            <Record>
                <AdmissionDate>2025-10-31</AdmissionDate>
                <Diagnosis>Flu</Diagnosis>
            </Record>
        </Patient>
    </Patients>
</Hospital>
```

Tips

- Choose meaningful element and attribute names.
- Keep XML well-formed: matching tags, proper nesting, and quoted attribute values.
- Optionally validate against a simple XSD if you want to practice schema validation.
