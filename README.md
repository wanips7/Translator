# Translator
Simple module for translation support

Translator - this is a global object that's created automatically.

Firstly, set localization path, then load localization file

```pascal
Translator.LocalesPath := 'D:\App\Locales';
 
Translator.TryLoadLocale('English.lng');
```
Then get a translation of something

```pascal
ButtonAddItem.Caption := Translator.Translate('Buttons', 'AddItem');
```
Or
```pascal
ButtonAddItem.Caption := Translate('Buttons.AddItem');
```
With formatting
```pascal
LabelTimeLeft.Caption := TranslateF('Labels.TimeLeft', [Seconds]);
```

The translation file is a .ini file, with .lng extension.

'Info' section is required. That's an example:

```ini
[Info]
Author=John
Icon=ICONBASE64STRING
Lang=English (USA)
Version=10

[Buttons]
AddItem=Add item
CheckConnection=Check connection

[Labels]
TimeLeft=Time left: %d seconds
```
