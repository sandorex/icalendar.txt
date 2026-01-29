# icalendar.txt
Simple calendar format in plain text that can contain all data icalendar format supports 

This is adapation of [todo.txt's](https://github.com/todotxt/todo.txt) philosophy

## The format
The format is quite simple, one event one line
```
<start> [<end>] [(<repeat>)] <description> @context +project custom_data:value
```

|Name|Format|Example|
|--|--|--|
|`<start>`|`ISO8601`|`2026-01-01T20:20`|
|`<end>`|`ISO8601` or `ISO8601 duration`|`2026-01-01T20:20` or `P7D20H`|
|`<repeat>`|`ISO8601 duration`|`P1D` to repeat every day|
|`<text>`||Pickup dry-cleaners|
|`@context`||@house|
|`custom_data:value`|`key:value`, where key and value can be anything without spaces or colons|`location:walmart`|

- If `<end>` is not specified then length is decided from `<start>` where `2015` would mean whole year `2015` and `2015-06` whole June of 2015

Some more examples so you get the idea
```
2026-01-28 (P7D) Take out garbage @chores
2026-02-10 (P1Y) John's birthday @birthdays
2026-02-16T10:00 P1H Meeting with Mike @work
2026-02-30 Shippment arrival @work
```

- [`ISO8601 format`](https://en.wikipedia.org/wiki/ISO_8601)
- [`ISO8601 duration format`](https://en.wikipedia.org/wiki/ISO_8601#Durations)

