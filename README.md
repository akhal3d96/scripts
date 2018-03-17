Those are some scripts I created or found that help me through the day bu automating laborious tasks.
I have no problem in contributing and improving the quality of the scripts but keep in mind those rules.
# Rules:
1. The language **must** be scripted. No binaries.
2. Here's the preferred languages in order of their preference:
    1. Bash (For its maximum portability)
    2. Ruby 
    3. Python
 3. Avoid external libraries (in case of Ruby and Python) or external programs (in case of Bash) as possible for maximum portability.
 4. In case you needed to import an external library or module (not per-installed with the default libraries). Check for it first, if it isn't installed, tell the user.
     ```python
       try:
         import gnupg
       except ModuleNotFoundError:
           print("python-gnupg isn't installed.\n")
           exit(-1)
     ```
5. Always check your script by a linter before submitting it:
    1. Bash: [ShellCheck](https://github.com/koalaman/shellcheck)
    2. Ruby: [RuboCop](https://github.com/bbatsov/rubocop)
    3. Python: [PyLint](https://github.com/PyCQA/pylint) 
  6. After the shebang, describe your script like this:
      ```ruby
      #!/bin/env ruby
      
      #: Title         : tashkeel_remover
      #: Date          : 22-08-2017
      #: Author        : "Ahmed Khaled" <nemoload@aol.com>
      #: Version       : 1.0
      #: Description   : Removes Arabic tashkeel characters
      #                     from a text passed as an argument.
      #: Options       : NONE
      ```
6. Don't add extension for the script (*.sh , *.rb , *.py)