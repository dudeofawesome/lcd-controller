# LCD Controller

A node module to control the Grove-LCD RGB Backlight Panel

# API

## Methods

### `setText(msg, pos, clear)`

* `msg` `(string)`
  * String to write to display
* `pos` `({x: number, y: number})`
  * Position to start writing string
* `clear` `(boolean)`
  * Whether or not the display should be cleared before writing string

### `clearText()`

Clears all text on display

### `setColor(red, green, blue)`

* `red` `(number)`
* `green` `(number)`
* `blue` `(number)`

Sets display backlight color

### `brighten()`

Tweens display backlight brightness from current brightness to 100% over a period of time

### `dim()`

Tweens display backlight brightness from current brightness to 0% over a period of time

### `setBrightness(brightness)`

* `brightness` `(number)`

Sets display backlight brightness
