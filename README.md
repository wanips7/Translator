# Translator
Simple module for translation support

Translator - this is a global object that's created automatically.

Firstly, set localization path, then load localization file

```
Translator.LocalesPath := 'D:\App\Locales';
 
Translator.TryLoadLocale('English.lng');
```
Then get a translation of something

```
ButtonAddItem.Caption := Translator.Translate('Buttons', 'AddItem');
```
Or
```
ButtonAddItem.Caption := Translate('Buttons.AddItem');
```

The translation file is a .ini file, with .lng extension.

'Info' section is required. That's an example:

```
[Info]
Author=John
Icon=ICONBASE64STRING
Lang=English (USA)
Version=10

[Buttons]
AddItem=Add item
CheckConnection=Check connection

[Messages]
Start=Start working
Stop=Stop working
```
