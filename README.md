# excel-cheat-sheet
Obvious and obscure Excel functionality for reference.

## Strings

### Length
I often find myself using the `LEN` function when mapping out tweets for social media strategies in Excel. The function returns the number of characters in a cell.
```
=LEN(cell)
```

## Math

### Sum
```
=SUM(range)
```

### Square Root
```
=SQRT(number)
```

Returns the positive square root of a positive number.

### Average

The `AVERAGE` function simply returns the average of the numbers in a particular range.
```
=AVERAGE(range)
```

Returns the average value from cells `A1` to `A10`.

## Rounding

### Round
```
=ROUND(number, places)
```
Rounds a `number` to a specified number of `places`.
- **number** The number that you want to round.
- **places** The number of places that you want to round to.

## Max & Min

### Max
```
=MAX(range)
```
Gives the maximum value from a range.

### Min
```
=MIN(range)
```
Gives the minimum value from a range.

## Relative vs. Absolute References
In Excel, Google Sheets, etc. there are two different types of references: relative and absolute.

### Relative References

If you copy a single cell across multiple cells, the references (e.g. `A1`) inside will change based on the relative position of the row and column of the new cell. For example:

| Input       | Output |
|-------------|--------|
| 1           | 1      |
| `=A1+1 `    | 2      |
| `=A2+1`     | 3      |
| `...`       | 4      |

In the example above, each cell will increment the previous cell by 1, as the `A1` becomes `A2` in the cell below it (the reference), and so on and so forth.

### Absolute References

When you copy a single cell across multiple cells, and, say, want to multiple everything by a constant value from another cell, you want to use an absolute reference, in order to avoid having to retype your constant everytime, or replace it if it changes.

Absolute references are denoted using the `$` token, and can placed in front of the column, row, or both. If the `$` token is placed in front of the column only, such as `$A1`, then all of the references will be relative to just the `A` column. Similarily, if the `$` token is placed in front of the row, such as `A$1`, then all of the references will be relative to just the first row.

For a true absolute reference, place the `$` token before **both** the column **and** the row: `$A$1`.

| Input       | Output |
|-------------|--------|
| 1           | 1      |
| `=$A$1+1 `  | 2      |
| `=$A$1+1 `  | 2      |
| `...`       | 2      |

When you copy the contents of the cell above, the `$A$1` reference will not be relative to the current cell cell.
