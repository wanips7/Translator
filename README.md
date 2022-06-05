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
