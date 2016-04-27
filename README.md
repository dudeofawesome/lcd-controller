# LCD Controller

A node module to control the Grove-LCD RGB Backlight Panel

# API

## Methods

### `setText(msg, pos, clear)`

* `msg` `(string)`
  * String to write to display
* `pos` `({x: number, y: number})`
  * Default: `{x: 0, y: 0}`
  * Position to start writing string
* `clear` `(boolean)`
  * Default: `true`
  * Whether or not the display should be cleared before writing string

### `clearText()`

Clears all text on display

### `getColor()`

Returns display backlight color

### `setColor(red, green, blue)`

* `red` `(number)`
* `green` `(number)`
* `blue` `(number)`

Tweens display backlight color from current color to new color

### `brighten()`

Tweens display backlight brightness from current brightness to 100% over a period of time

### `dim()`

Tweens display backlight brightness from current brightness to 0% over a period of time

### `getBrightness()`

Returns display backlight brightness

### `setBrightness(brightness)`

* `brightness` `(number)`

Sets display backlight brightness

# Limitations
* The LCD panel becomes unstable when receiving messages faster than 40 times a second. Because of this, I've implemented a queue that will ensure messages are only sent up to 40 times per second. If you fill it with more than 40 commands in a second, then your commands will potentially be delayed. Remember, any backlight commands using tweens will likely send more than 1 command!
