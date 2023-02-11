# Top 10 words in the Declaration of Independence

## Get the file
```
wget https://web.math.princeton.edu/~perezgiz/usdec.txt
```

## Solution
```
tr A-Z a-z < usdec.txt | tr -d ":,.\t"| tr ' ' '\n' | sort | uniq -c | sort -nr | head -10 | tee  usdechistogram.txt
```

### Workflow
- Convert upper case to lower case
- Delete unnecessary characters
- Replace new lines with space
- Sort lines based on first character
- Count number of occurences of each line
- Sort words by numerical value in descending order
- Get top 10 lines
- Output to file specified and stdout




