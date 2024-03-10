# GitHub Markdown Table of Contents Generator
This is a convenient _(at least for me)_ markdown ToC generator.

## Installation and Usage
- Download the script:
```bash
wget https://raw.githubusercontent.com/maksyche/github-md-toc-generator/master/toc_generator.py
```
- Run it:
```bash
python3 toc_generator.py
python3 toc_generator.py -d # Run with DEBUG log level
```

## Results
- _**IMPORTANT**_: The script adds ToC to the files right below the lvl1 heading. _**Everything between the lvl1 and the 
first lvl2 headings is replaced with the ToC**_.
- Check [this example](example.md):
```markdown
# Lvl1
* [Lvl2 with . a dot](#lvl2-with--a-dot)
    * [Lvl3 with an _underscore](#lvl3-with-an-_underscore)
    * [Lvl3 with _underscores_](#lvl3-with-underscores)
* [Lvl2 with a *star](#lvl2-with-a-star)
* [Lvl2 with *stars*](#lvl2-with-stars)
* [Lvl2 with `./inline-code`](#lvl2-with-inline-code)
    * [Lvl3 `_with _underscores_` inside and outside_ of code](#lvl3-_with-_underscores_-inside-and-outside_-of-code)
        * [Lvl4](#lvl4)
            * [Lvl5](#lvl5)
                * [Lvl6](#lvl6)
* [Lvl2 with a ~tilda](#lvl2-with-a-tilda)
* [Lvl2 with a +plus](#lvl2-with-a-plus)
* [Lvl2 with an 'apostrophe](#lvl2-with-an-apostrophe)

## Lvl2 with . a dot
### Lvl3 with an _underscore
### Lvl3 with _underscores_
## Lvl2 with a *star
## Lvl2 with *stars*
## Lvl2 with `./inline-code`
### Lvl3 `_with _underscores_` inside and outside_ of code
#### Lvl4
##### Lvl5
###### Lvl6
####### There's no lvl7
## Lvl2 with a ~tilda
## Lvl2 with a +plus
## Lvl2 with an 'apostrophe
```

## Ignore Files
- Create the `.tocignore` file in the current folder.
- Put some regex patterns for files and folders that should be ignored. Currently, only regex patterns are supported 
_(no `ignorelang` for now)_. Example:
```ignorelang
README.md
somefile.md
somefolder/+.*
someotherfolder/someotherfile.md
```


