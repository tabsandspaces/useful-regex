# useful-regex

Websites like [RegExr](http://regexr.com) or text editors like [Atom](http://atom.io) allow to find sequences of characters that match a regular expression. Here are some regex-patterns you might find useful when working with subtitles.


#### Match groups of more than 45 characters
It also works for the lines containing a vertical bar divider.

```(?:(?!(\||\n)).){45,}```

#### Match common timecodes
Be careful with subtitles containing nothing but a number as these may get lost in some special cases.

```\d{0,}?\n{0,}?\s{0,}?(\d{1,2}[,.:]){3}\d{1,3}\s{0,}-?-?>?\s{0,}(\d{1,2}[,.:]){3}\d{1,3}```

To delete the timecodes, just replace found character groups with nothing. After some additional formatting, you will get pure text.

#### Match trailing spaces
It's always good not to have them.

```^[ \t]+|[ \t]+$```

_Enable multiline flag for this._

#### Match HTML tags
...or anything between angle brackets.

```\<[^\>]*\>```
