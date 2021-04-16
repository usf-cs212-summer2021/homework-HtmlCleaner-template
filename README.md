HtmlCleaner
=================================================

![Points](../../blob/badges/points.svg)

For this homework, you will "clean" HTML leaving only the core text behind. This includes converting or removing HTML entities, removing HTML tags and comments, and removing some HTML block elements.

#### Handling Entities ####

[HTML entities](https://developer.mozilla.org/en-US/docs/Glossary/Entity) are how special characters are encoded in HTML. For example, the entity `&amp;copy;` renders as &copy; in HTML and is the `©` Unicode character.

Each HTML entity should be converted from the HTML representation to its Unicode character when possible using the [StringEscapeUtils.unescapeHtml4](https://commons.apache.org/proper/commons-text/javadocs/api-release/org/apache/commons/text/StringEscapeUtils.html#unescapeHtml4(java.lang.String)) method of the [Apache Commons Text](https://commons.apache.org/proper/commons-text/) third-party library. Any entities that cannot be converted must then be removed. 

## Hints ##

Below are some hints that may help with this homework assignment:

  - View the Javadoc comments using the "Javadoc" view in Eclipse. It will render the HTML in the comments properly.

  - Each method can be completed using a combination of regular expressions and the [`String.replaceAll`](https://docs.oracle.com/en/java/javase/15/docs/api/java.base/java/lang/String.html#replaceAll(java.lang.String,java.lang.String) method.
  
  - You will have to generate a regular expression for the `HtmlCleaner.stripElement` method based on the element name provided as a parameter. It can be helpful to use Java [format strings](https://docs.oracle.com/en/java/javase/15/docs/api/java.base/java/util/Formatter.html) for this, but it is not required.

*Note:* Before using these classes with project 4, you will need to make some modifications. Specifically, you will eventually need to make your `LinkParser` and `HtmlCleaner` work together so that you parse links after stripping block elements, but before stripping tags and entities. (This is not required for the homework, however.)

## Resources ##

We do not extensively cover HTML in this class. However, there are many helpful resources on the web for more about this markup language. Some resources include:

  - [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML)
  - [W3C Markup Validation](https://validator.w3.org/)
  - [Web Design Group](https://htmlhelp.com/)

## Requirements ##

See the Javadoc and `TODO` comments in the template code in the `src/main/java` directory for additional details. You must pass the tests provided in the `src/test/java` directory. Do not modify any of the files in the `src/test` directory.

See the [Homework Guides](https://usf-cs212-spring2021.github.io/guides/homework/) for additional details on homework requirements and submission.
