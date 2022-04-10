# pico-micropython-lcd1602
micropython library for interfacing # 1602 displays with rpi pico (using d4-d7)

sry i wrote pretty fast, its todo...

### How to Use
You need to upload `lcd1602.py` to rpi pico. If you are using [pico-go](https://marketplace.visualstudio.com/items?itemName=ChrisWood.pico-go), copy this file to your program folder, open it & click upload button on bottom of vscode.

### Example Program
This is very easy sample program
```python
# import library
from lcd1602 import lcd1602

# init display & disable cursor
display = lcd1602(rs, e, d4, d5, d6, d7)
display.cursor(False)

# clear display
display.clear()

# write to second row
display.position(1, 0)
display.write("Hello World!")
```

### All Funtions
* `clear()`
  * clear screen
* `home()`
  * move cursor to 0, 0
* `cursor(blink, underscore)`
  * blink - enable or disable cursor visibility
  * underscore - change visibility from square to underscore
* `write(data)`
  * write to screen
* `position(row, col)`
  * row - 0 or 1, row number
  * col - 0 to 15, character in row
* `character(id, data)`
  * [more here](https://mil.ufl.edu/3744/docs/lcdmanual/commands.html)
  * id - id of custom character
  * data - byte array
