Initialization: const colorlib = ColorLib()

<br/>

>colorlib.get_dominant(image, palette_size=1, use_limits=false)

This gets the dominant color or colors of an image.<br/> 
Palette size is the number of colors to return.<br/>
If use_limits is true it will ignore colors when r, g, and b are below 10 or above 245.

<br/>

>colorlib.get_lighter_or_darker(rgb, amount=0.2)

This returns a darker color if the color is considered light,<br/>
or a lighter color if the color is considered dark.<br/>
rgb is an array like [0, 20, 5].<br/>
amount specifies how much darker or lighter it gets.

<br/>

>colorlib.is_light(rgb)

Checks if a color is considered light.<br/>
Receives an rgb array.

<br/>

>colorlib.is_dark(rgb)

Checks if a color is considered dark.<br/>
Receives an rgb array.

<br/>

>colorlib.get_proper_font(rgb)

Used to give a proper font color to a background color.<br/>
If color is light it returns #000000.<br/>
If color is dark it returns #ffffff.<br/>
Although it's advised to use get_lighter_or_darker to achieve more natural contrasts.

<br/>

>colorlib.array_to_rgb(array)

Transforms an rgb array like [x, y, z] into rgb(x, y, z).<br/>
An array with multiple array arguments can be passed.

<br/>

>colorlib.rgb_to_array(rgb)

Transforms rgb(x, y, z) to [x, y, z].<br/>
An array with multiple rgb arguments can be passed.

<br/>

>colorlib.rgb_to_rgba(rgb, alpha)

Replaces rgb(x, y, z) to rgba(x, y, z, alpha).

<br/>

>colorlib.rgba_to_rgb(rgb, alpha)

Replaces rgba(x, y, z, alpha) to rgb(x, y, z).

<br/>

>colorlib.rgb_to_hex(rgb, hash=true)

This turns an array to a hex string.<br/>
If an rgb string is given it will convert it to an array automatically.</br>
For instance [1,2,3] or "rgb(1, 2, 3)" will turn to "#010203",</br>
If hash is false it won't add the # to the string.

<br/>

>colorlib.hex_to_rgb(hex)

This turns a hex string to an rgb array.<br/>
For instance "#010203" or "010203" will return [1,2,3],

<br/>

>colorlib.check_array(array)

Checks if an rgb array is composed of valid values.<br/>
A valid value is between 0 and 255.<br/>
If a value is not in that range it is fixed.<br/>
This returns a valid array, not true or false.

<br/>

>colorlib.check_rgb(rgb)

This checks if rgb is an array.<br/>
If not, an array is created and returned.<br/>
rgb(0, 1, 2) would return [0, 1, 2].