# useful-regex
Some useful regular expressions for working with subtitles


Match lines with more than 45 characters:
```(?:(?!(\||\n)).){45,}```

Match common timecodes (be careful with subtitles containing nothing but a number):
```\d{0,}?\n{0,}?\s{0,}?(\d{1,2}[,.:]){3}\d{1,3}\s{0,}-?-?>?\s{0,}(\d{1,2}[,.:]){3}\d{1,3}```

Match trailing spaces _(enable multiline flag)_:
```^[ \t]+|[ \t]+$```

Match HTML tags (or anything between angle brackets):
```\<[^\>]*\>```
