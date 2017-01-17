# Class_DD
[DD](http://www.ddxoft.com/) is a virtual keyboard/mouse library, used to simulate keys/mouse in hardware driver level.

## Limitation
A network connection is required when loading the DD library (dll file), but once loaded the computer can go offline.
The author of DD provides a paid service for removing the network requirement, you can mail him at [this](mailto:2827362732@qq.com) address.

## Methods

* **btn(param)** - Simulate mouse button press
```
param:   1 = LButton Down,    2 = LButton Up
         4 = RButton Down,    8 = RButton Up
        16 = MButton Down,   32 = MButton Up
        64 = Button 4 Down, 128 = Button 4 Up
       256 = Button 5 Down, 512 = Button 5 Up
```
* **mov(x, y)** - Simulate mouse move

* **movR(dx, dy)** - Simulate mouse move (relatively)

* **whl(param)** - Simulate mouse wheel
```
param: 1=upward 2=downward
```

* **key(param1, param2)** - Simulate keyboard
```
param1: DD code
param2: 1=Down 2=Up
```

* **todc(VKCode)** - VKCode to DD code

* **str(string)** - Send string

----
Some helper methods:
* **_btn(sNick)**
```
sNick: One of the following
	LButtonDown, LButtonUp
	RButtonDown, RButtonUp
	MButtonDown, MButtonUp
	4ButtonDown, 4ButtonUp
	5ButtonDown, 5ButtonUp
```

* **_key(sKey, sflag)**
```
sKey: The key name
sflag: Down or Up
```
*Example: _key("F11", "Down")*

* **_key_press(sKey)**
```
sKey: The key name
```
* **_whl(sParam)**
```
sParam: Down or Up
```

## Usage Example
```AutoHotkey
#Include, class_DD.ahk

DD.str("abc")
DD._key_press("F11")
```
