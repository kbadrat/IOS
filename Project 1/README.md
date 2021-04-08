~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~FAKULTA   INFORMAČNÍCH   TECHNOLOGIÍ   VUT   V   BRNĚ~~~~~~~~~~~~~~~~~~~~~~~~~~~~
IOS 2020/21: Projeсt 1
The author is Vladislav Kovalets, xkoval21
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
This is a script for analyzing the record of a stock trading system.
The script filters records and provide statistics according to user input.
If a command is also given to the script, it executes the command over the filtered records.
If the script does not receive a filter or command, it copies the records to standard output
It can also process records compressed with the gzip tool (if the file name ends in .gz).
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
A log format must be as follows: DATE AND TIME; TICKER; TYPE OF TRANSACTION; UNIT PRICE; CURRENCY; VOLUME; ID
For example: 2021-07-29 23:43:13;TSM;buy;667.90;USD;306;65fb53f6-7943-11eb-80cb-8c85906a186d
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
Usage: tradelog [-h|--help] [FILTER] [COMMAND] [LOG [LOG2 [...]]
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
The COMMAND can be one of:

list-tick   – a list of occurring stock exchange symbols, so-called "ticker".
profit      – statement of total profit from closed positions.
pos         – a list of values of currently held positions sorted in descending order by value.
last-price  – listing the last known price for each ticker.
hist-ord    – statement of the histogram of the number of transactions according to the ticker.
graph-pos   – statement of the graph of values of held positions according to the ticker.
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
The FILTER can be a combination of the following:

-a DATETIME – after: only records after this date are considered (without this date).
-b DATETIME – before: only records before this date are considered (without this date).
              DATETIME is in the format \"YYYY-MM-DD HH:MM:SS\".
-t TICKER   – only entries corresponding to a given ticker are considered.
              With multiple occurrences of the switch, the set of all listed ticker is taken.
-w WIDTH    – in the list of graphs, it sets their width, that is, the length of the longest line to width.
              Thus, WIDTH must be a positive integer. Multiple occurrences of the switch is a faulty start.
–––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
Copyright 2021
This program is free software. You can redistribute it and/or modify it
This program is distributed in the hope that it will be useful.
