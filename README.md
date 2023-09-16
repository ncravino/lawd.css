# Lawd.css

"Simply the BESTiest CSS libary for text" \- a notourious chonky cat somewhere  

A minimalist CSS library using variables (see bellow) to do:
- [Chonkyness](#chonkyness): 10 ```font-size``` classes.
- [Notouriousnes](#notouriousness): 2 text border sizes classes using a shadow, for visibility of text over mixed coloured backgrounds.
- [Cuddliness](#cuddliness): 2 ```line-height``` classes.

## License

This library is licensed under a BSD-3-Clause [License](./LICENSE).

## Using

Simply use the ```./css/lawd.css``` file from [https://github.com/ncravino/lawd.css](https://github.com/ncravino/lawd.css) together with other libraries. I like to use it with [chota.css](https://jenil.github.io/chota/), which is great for a modern minimalist CSS lib for grids and some styling.

## Chonkyness
These classes allow you to change the size of the text, relative to ```--default-chonk-size```.
The text size for ```head```, ```body```. ```h1-6``` will also be set when including the ```lawd.css``` file.

- ```.tiny``` will set the ```font-size``` to ```--default-chonk-size``` minus ```0.3rem```.
- ```.thin``` will set the ```font-size``` to ```--default-chonk-size``` minus ```0.2rem```.
- ```.fine``` will set the ```font-size``` to ```--default-chonk-size``` minus ```0.1rem```.
- ```.chonk``` will be equal to ```--default-chonk-size```, html and body will also be set to this size.
- ```.heckinchonker``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.1rem```,
    h6 will also be set to this size.
- ```.heftychonk``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.2rem```, h5 will
    also be set to this size.
- ```.megachonk``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.3rem```, h4 will
    also be set to this size.
- ```.gojira``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.4rem```, h3 will
    also be set to this size.
- ```.moonface``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.5rem```, h2 will
    also be set to this size.
- ```.ohlawd``` will set the ```font-size``` to ```--default-chonk-size``` plus ```0.6rem```, h1 will also be
    set to this size.

## Notouriousness
These classes allow you to add a border around each letter, in order to make it stand against backgrounds that have a mix of light and dark colours.
You can change the color overriding ```--default-notoriousness-colour``` which is ```rgba(128,128,128,0.5)``` by default, see variables bellow for more info.

- ```.notorious``` will add a ```var(--default-cuddle-cuddliness)```border using shadow around each letter. The default is 1px.
- ```.blatant``` will add a ```var(--default-blatant-cuddliness)``` border using shadow around each letter. The default is 1.5px.

## Cuddliness

These classes allow you to change the ```line-height```.
The ```line-height``` set on import for ```body``` and ```html``` is ```--default-chonk-height``` which defaults to ```var(--default-chonk-size) + 0.2rem```.

- ```.cuddly``` will change ```line-height``` to ```--default-cuddly-cuddliness```
    which defaults to ```1em```.
- ```.itfits``` will change ```line-height``` to ```--default-itfits-cuddliness```
    which defaults to ```0.85em```.

## CSS Variables

You can/should override any of the following variables:

- ```--default-chonk-size``` sets the ```font-size```, default is ```1.1rem```
- ```--default-chonk-height``` sets the ```line-height```, default is .```--default-chonk-size + 2rem```.
- ```--default-notoriousness``` sets the amount of pixels used by the shadow in ```.cuddly``` .
- ```--default-thin-notoriousness``` sets the amount of pixels used by the shadow in ```.itfits```.
- ```--default-notoriousness-colour``` sets the colour of the shadow used by ```.cuddly``` and ```.itfits```, default is ```rgba(128, 128, 128, 0.5)```.
- ```--default-cuddle-cuddliness``` sets the ```line-height``` for ```.cuddly```, default is ```1em``` .
- ```--default-itfits-cuddliness``` sets the ```line-height``` for ```.itfits```, default is ```0.85em```.

The following variables can be overriden but may cause unexpectedly funny results:
- ```--default-negative-notoriousness``` sets negative shadow pixels for ```.cuddly```, automatically computed from ```calc(0px - var(--default-notoriousness))```.
- ```--default-negative-thin-notoriousness``` sets negative shadow pixels for ```.itfits```, automatically as ```calc(0px - var(--default-thin-notoriousness))```  .

### How to override?

Just create a ```:root``` element in a custom css file included after ```lawd.css``` and define what you want to change there, e.g.:
```
:root {
    --default-chonk-size: 2rem;
}
```