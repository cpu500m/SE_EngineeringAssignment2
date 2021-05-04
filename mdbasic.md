# __Basic Syntax__
### The Markdown elements outlined in John Gruber's design document.
<br>

___
___
<Br>

## **Overview**
### Nearly all Markdown applications support the basic syntax outlined in John Gruber’s original design document. There are minor variations and discrepancies between Markdown processors — those are noted inline wherever possible.
<br>

___
<br>

## **Headings**
### To create a heading, add number signs (#) in front of a word or phrase. The number of number signs you use should correspond to the heading level. For example, to create a heading level three(\<>) , use three number signs (e.g., ### My Header).
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|# Heading level 1|\<h1>Heading level 1\</h1>|<h1>Heading level 1
|## Heading level2|\<h2>Heading level 2\</h2>|<h2>Heading level 2
|### Heading level 3|\<h3>Heading level 1\</h3>|<h3>Heading level 3
|#### Heading level4|\<h4>Heading level 2\</h4>|<h4>Heading level 4
|##### Heading level 5|\<h5>Heading level 1\</h5>|<h5>Heading level 5
|###### Heading level6|\<h6>Heading level 2\</h6>|<h6>Heading level 6 
<br>

___
<br>

## **Alternate Syntax**
### Alternatively, on the line below the text, add any number of == characters for heading level 1 or -- characters for heading level 2.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|Heading level 1<br>===========|\<h1>Heading level 1\</h1>|<h1>Heading level 1
|Heading level2<br>------------------|\<h2>Heading level 2\</h2>|<h2>Heading level 2<br>______________________
<br>

___
<br>

## **Heading Best Practices**
### Markdown applications don’t agree on how to handle a missing space between the number signs (#) and the heading name. For compatibility, always put a space between the number signs and the heading name.


|✅ DO this|❌Don't do this|
|:--|:--|
|<h2># Here's a Heading|<h2>#Here's a Heading|
<br>

___
<br>

## **Paragraphs**
### To create paragraphs, use a blank line to separate one or more lines of text.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|I really like using Markdown.<br><br>I think I'll use it to format all of my documents from now on.|\<p>I really like using Markdown.\</p><br><br>\<p>I think I'll use it to format all of my documents from now on.\</p>|I really like using Markdown.<br><br>I think I'll use it to format all of my documents from now on.
<br>

___
<br>

## **Paragraph Best Practices**
### Unless the paragraph is in a list, don’t indent paragraphs with spaces or tabs. (I replace blank with _.)
|✅ DO this|❌Don't do this|
|:--|:--|
|Don't put tabs or spaces in front of your paragraphs.<br><br>Keep lines left-aligned like this.|______This can result in unexpected formatting problems.<br><br>_______Don't add tabs or spaces in front of paragraphs.
<br>

____
<br>

## **Line Breaks**
### To create a line break (\<br>), end a line with two or more spaces, and then type return.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|This is the first line.<br>And this is the second line.|\<p>This is the first line.\<br><br>And this is the second line.\</p>|This is the first line.<br>And this is the second line.
<br>

___ 
<br>

## **Line Break Best Practices**
### You can use two or more spaces (commonly referred to as “trailing whitespace”) for line breaks in nearly every Markdown application, but it’s controversial. It’s hard to see trailing whitespace in an editor, and many people accidentally or intentionally put two spaces after every sentence. For this reason, you may want to use something other than trailing whitespace for line breaks. Fortunately, there is another option supported by nearly every Markdown application: the \<br> HTML tag.
<br>

### For compatibility, use trailing white space or the \<br> HTML tag at the end of the line.
<br>

### There are two other options I don’t recommend using. CommonMark and a few other lightweight markup languages let you type a backslash (\) at the end of the line, but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. And at least a couple lightweight markup languages don’t require anything at the end of the line — just type return and they’ll create a line break.
|✅ DO this|❌Don't do this|
|:--|:--|
|First line with two spaces after.<br>And the next line.<br><br>First line with the HTML tag after.\<br><br>And the next line.|First line with a backslash after.\\<br>And the next line.<br><br>First line with nothing after.<br>And the next line.

<br>

___
<br>

# ***Emphasis***
### You can add emphasis by making text bold or italic.
<br>

## **Bold**
### To bold text, add two asterisks or underscores before and after a word or phrase. To bold the middle of a word for emphasis, add two asterisks without spaces around the letters.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|I just love \*\*bold text**.|I just love \<strong>bold text\</strong>.|I just love **bold text**.
|I just love \_\_bold text__.|I just love \<strong>bold text\</strong>.|I just love __bold text__.
|Love\*\*is**bold|Love\<strong>is\</strong>bold|<h2>Love**is**bold

<br>

___
<br>

## **Bold Best Practices**
### Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold the middle of a word for emphasis.
|✅ DO this|❌Don't do this|
|:--|:--|
|<h2>Love\*\*is**bold|<h2>Love__is__bold

<br>

___
<br>

## **Italic**
### To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|Italicized text is the \*cat's meow*.|Italicized text is the \<em>cat's meow\</em>.|<h2>Italicized text is the *cat’s meow*.
|Italicized text is the \_cat's meow_.|Italicized text is the \<em>cat's meow\</em>.|<h2>Italicized text is the _cat’s meow_.
|A\*cat*meow|A\<em>cat\</em>meow|<h2>A*cat*meow

<br>

___
<br>

## **Italic Best Practices**
### Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to italicize the middle of a word for emphasis.
|✅ DO this|❌Don't do this|
|:--|:--|
|<h2>A\*cat*meow|<h2>A_cat_meow

<br>

___
<br>

## **Bold and Italic**
### To emphasize text with bold and italics at the same time, add three asterisks or underscores before and after a word or phrase. To bold and italicize the middle of a word for emphasis, add three asterisks without spaces around the letters.
|Markdown|HTML|Rendered Output|
|:--|:--|:--|
|This text is \*\*\*really important***.|This text is \<strong>\<em>really important\</em>\</strong>.|<h2>This text is ***really important***.
|This text is \_\_\_really important___.|This text is \<strong>\<em>really important\</em>\</strong>.|<h2>This text is ___really important___.
|This text is \*\*\_really important_**.|This text is \<strong>\<em>really important\</em>\</strong>.|<h2>This text is **_really important_**.
|This text is \_\_\*really important*__.|This text is \<strong>\<em>really important\</em>\</strong>.|<h2>This text is *__really important__*.
|This is really\*\*\*very***important text.|This is really\<strong>\<em>very\</em>\</strong>important text.|<h2>This is really***very***important text.

<br>

___