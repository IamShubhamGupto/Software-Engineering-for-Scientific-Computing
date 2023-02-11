# Top 10 words in the Declaration of Independence

## Get the file
```
wget https://web.math.princeton.edu/~perezgiz/usdec.txt
```

## Solution
```
tr 'A-Z\n' 'a-z ' < usdec.txt | tr -d ":,.;\t" | tr -cs "[:alpha:]" "\n" | sort | uniq -c | sort -rn | head -10 | tee usdechistogram.txt
```

### Workflow
- Convert upper case to lower case and replace new line with spaces
- Delete unnecessary characters
- Print one word per line
- Sort lines based on first character
- Count number of occurences of each line
- Sort words by numerical value in descending order
- Get top 10 lines
- Output to file specified and stdout




