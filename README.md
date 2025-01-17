# RegExHotstrings

Provides RegEx in hotstring triggering like normal hotstring.

Use `Space`, `Tab` or `Enter` to trigger RegExHotstring.

## Usage

`RegExHotstring(String, CallBack, Options)`

- String:
  - [RegEx string](https://www.autohotkey.com/docs/v2/misc/RegEx-QuickRef.htm)
- CallBack:
  - calls function with [RegExMatchInfo](https://www.autohotkey.com/docs/v2/lib/RegExMatch.htm#MatchObject) as argument and clear string that triggers it
  - RegExReplace string, works like [RegExReplace](https://www.autohotkey.com/docs/v2/lib/RegExReplace.htm)
- Options:
  - \* (asterisk): An ending character (e.g. Space, Tab, or Enter) is not required to trigger the hotstring.
  use *0 to turn this option back off.

  - ? (question mark): The hotstring will be triggered even when it is inside another word;
  that is, when the character typed immediately before it is alphanumeric.
  Use ?0 to turn this option back off.

  - B0 (B followed by a zero): Automatic backspacing is not done to erase the abbreviation you type.
  Use a plain B to turn backspacing back on after it was previously turned off.

  - C: Case sensitive: When you type an abbreviation, it must exactly match the case defined in the script.
  Use C0 to turn case sensitivity back off.

  - O: Omit the ending character of auto-replace hotstrings when the replacement is produced.
  Use O0 (the letter O followed by a zero) to turn this option back off.

## Limitations

- incompatible with `#IfWin` or `#HotIf`
- unable to match white space characters and word boundaries (or anything related to that)
