# Streamm
Streamm is a programming language based on streamms, STDOUT is a stream, STDIN is a stream, the only data type is a stream, for example a "Hello" program (Hello World is hard):

    Hello!|,
    
Basically, each line has 2 parts, the value and the name, formatted `value|name`. The special name `,` means STDOUT, and the value Hello! means to write Hello! to STDOUT

# Interpreter
There is currently no interpreter for this language.

# Is that it?
No. Thanks to *filters*, Streamm isn't as boring as it seems:

    HiHiHi|,^{
      %pos|currentPos // %X means attribute X of the copying process, as the value is copied to the name, it checks this code block to make sure the character is valid
      currentPos mod 2|posMod2
      BE posMod2 // BE means return, if currentPos is even, then return 0, otherwise return 1, so only copy every other character
    }

Output: `iii`
