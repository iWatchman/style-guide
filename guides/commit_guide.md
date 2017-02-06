# Commit Etiquette
General Etiquette for Commits

## Commit Emojis
There's this cool thing where you can embed emojis into your git commit messages. At work, we have an established list of emojis for different types of edits to the repository. This makes it easy to navigate commit history and identify what anyone has been doing.

### General Edits
- :art: General file changes `:art:`
- :tada: Add new functionality `:tada:`
- :memo: Update/add comments to a file `:memo:`
- :skull: Adding skeleton files outlining code functionality `:skull:`

### Refactoring
- :bug: Bug fixes `:bug:`
- :truck: Rename/move files `:truck:`
- :fire: Delete code `:fire:`

### Assets
- :camera: Add assets (images, graphs, etc.) `:camera:`

## Language
Use the present tense, active voice to begin all commit messages. If you're wondering if it's right or not, think of the commit message as the second part of the sentence beginning with `If I pull this commit, it will...` or `This commit will...`. For example:
```
Add main script skeleton file
Fix bug causing divide by zero error
Move asset files to /assets directory
```

## Length
It's general curtesy to keep the first line of your commit message under 50 characters in length. If you have more to say, keep the first line short and general, hit `enter` twice, then continue to write as much as you want. The purpose of keeping the first line under 50 characters is so that the message displays nicely in commit history listings. For example:
```
:bug: Fix bug causing divide by zero error

In certain conditions, myFunc would introduce a rounding error in calculating the denominator,
resulting in a value of zero, thus the error.
```

## Usage
When writing your commit message, place the emoji at the very beginning of the message, then continue your message normally. Be sure to separate the emoji from your message with a space. For example:
```
:fire: Remove excess for loops in myFunc
```
