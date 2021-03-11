# Languages for the Carbon Class project
The Carbon Class applications allow you to display it in multiple languages. We acomplish this using so called language files. A language file is a file in the JSON format, that contains all the text the application uses in the selected language. More information about JSON can be found [here](https://www.w3schools.com/whatis/whatis_json.asp).
## Editing and bug reports 
If you find any problem with translation, a misspelled word or now a language and want to create a new translation, there are two main ways you report this. Pull Requests or Issues.
### Issues
An issue is the simpler form. You can just create an issue (Click the issues tab and then new issue) and write your complaint there. Issues can take a while to review and more time to fix the problem, but if you don't feel like doing much else, then an issue is the right choice.
### Pull Requests 
Pull Request is a report of a problem, that directly proposes a fix. If you're not familiar with git pull requests, you can find more information [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests). As pull request directly propose a fix, they are usually reviewed fairly quickly. 
## File structure
If you're looking to make a pull request or just want to read the language files, you may want to know, how the files in this repo effect the end application and how they are structured. 
### All.json
The `all.json` file is the main file of the repo. It contains a JSON array of strings. These strings represent language codes, that are currently supported. If the language code is ot in the all.json file, then there is either no translation, or the translation is incomplete.
How the all.json file might look:  
`all.json`  
```json
[
  "en",
  "cs",
  "de",
  "fr"
]
```
This file would indicate, that there are functional languages - English, Czech, German and French 
### The Language file
The language file contains the texts themselves. Filename of the language is always the language code (the one provided in the `all.json` file) and the `.json` suffix. Each of the language files contain a JSON object. The keys of this JSON objects (on the left of the colon) are the same across all languages - they tell the application where this text should be used. The values (on the right of the colon) are the transslations - they differ across languages.  
An expamle of an `en.json` file could look like this:  
`en.json`
```json
{
  "test": "This is a testing text."
}
```
This file contains only one entry (one text) with the key `"test"` and value (in english) `"This is a testing text."`.
An expamle of this file translated to German would look something like this:  
`de.json`  
```json
{
  "test": "Dies ist ein Testtext."
}
```
