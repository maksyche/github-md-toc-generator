# GitHub Markdown Table of Contents generator
This is a convenient _(at least for me)_ python wrapper for the [gh-md-toc](https://github.com/ekalinin/github-markdown-toc).
Generates TOC for markdown files in the current folder and subfolders.

## Installation and usage
- Download [gh-md-toc](https://github.com/ekalinin/github-markdown-toc).
- Download the script:
```bash
wget https://raw.githubusercontent.com/maksyche/github-md-toc-generator/master/toc_generator.py
```
- Run it:
```bash
python3 toc_generator.py
python3 toc_generator.py -d # Run with DEBUG log level
```
- The script adds TOC to the files right between the lvl1 and the first lvl2 headings. Example:
```markdown
# Lvl1 heading
   * [Lvl2 heading](#lvl2-heading)
      * [Lvl3 heading](#lvl3-heading)
   * [Another lvl2 heading](#another-lvl2-heading)

## Lvl2 heading
### Lvl3 heading
## Another lvl2 heading
```
- IMPORTANT: Everything between the lvl1 and the first lvl2 headings is replaced with the TOC.

## Ignoring files
- Create the `.tocignore` file in the current folder.
- Put some regex patterns for files and folders that should be ignored. Currently, only regex patterns are supported _(no ignorelang for now)_. Example:
```ignorelang
somefile.md
somefolder/+.*
someotherfolder/someotherfile.md
```


