# How to add a translation in your language
To add a translations in other language, please follow this steps:

First, create the Portable Object (.po) for your language
```
msginit --input=po/messages.pot --locale=LANG_CODE --output=po/LANG_CODE/messages.po
```
A new po/LANG_CODE/messages.po file should appeared.
Now you can translate the strings in the program:
```
#: example_file.c:12
#, c-format
msgid "Original text\n"
msgstr "Translated text\n"
```
The last step is to generate the .mo file:
```
msgfmt --output-file=po/LANG_CODE/LC_MESSAGES/messages.mo po/LANG_CODE/messages.po
```

Note you should change LANG_CODE to your language code

Credits for: [http://www.labri.fr](http://www.labri.fr/perso/fleury/posts/programming/a-quick-gettext-tutorial.html)