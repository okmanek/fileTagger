this application was created to enable tagging files on linux on filesystem not adapted to tagging (e.g. ext4). I checked some existing programs 

and I wasn't quite content with what they offered:
-tagsistant - usability, syntax were not good
-TMSU - written in Go so I couldn't contribute without learning this language, also syntax wasn't as good as it could be

The assumption was to create tool which simplicity was inspired by git. Therefore, in every affected folder we create file (not directory, we don't need those) called ".tags"

note: it's better to alias app name to something shorter, e.g.:
alias t="taggger"

syntax:
  creating new tag:
    tagger newTag <tag name 1> <tag name 2> <...> <tag name n>
    tags are global and stored in ~/.tagger.txt

  adding tags:
    tagger <filename> <tag 1> <tag 2> <...> <tag n>
    or
    tagger <filename> <tag 1> <tag 2> <...> <tag n>

  list file tags:
    tagger <filename>
  list files in directory with their tags:
    tagger ls

  removing tags:
    tagger <filename> - <tag 1> <tag 2> <...> <tag n>
  searching tags:
    ...
  help:
    tagger help|-h|--help


tagging directories: TBD
backuping tags, or storing them in central place instead of 1 for every folder: TBD
czy na pewno tagi powinny byc globalne?
merging tags: TBD
