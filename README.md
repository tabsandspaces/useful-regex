# useful-regex
Some useful regular expressions for working with subtitles


Match lines with more than 45 characters:
```(?:(?!(\||\n)).){45,}```

Match SRT timecodes:
```\d{1,}?\n{1,}?([0-9]{1,2}[,.:]){3}[0-9]{1,3}\s{0,}-?-?>?\s{0,}([0-9]{1,2}[,.:]){3}[0-9]{1,3}```

Match trailing spaces _(enable multiline flag)_:
```^[ \t]+|[ \t]+$```

Match HTML tags (or anything between angle brackets):
```\<[^\>]*\>```
