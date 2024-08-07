# mvmify
mvmify is a humorous utility meant to turn the entirety of your C or C++ code into permutations of the word 'mvm'.

Inspired by [this reddit post](https://www.reddit.com/r/ProgrammerHumor/comments/bgdxwn/yeet/).

## Installation
First, the executable must be built, which can be done by simply calling `g++ mvmify.cpp -o mvmify`. Once you compile, make sure to move the executable to your PATH.

## Usage
To use mvmify, simply call `mvmify file_path`, as long as the path is to a .c, .cc, or.cpp file. This will work best if the file has spaces between each individual token (e.g. brackets, operators, keywords, etc.), but will still work as long as there are no multiple-word quotes. 

## How it works
The program iterates line-by-line, ignoring all `using`, `#define` or `#include` macros. It takes in each unique word/token and pairs it with a randomly generated permutation of the word 'mvm'. It then makes a copy of the original file and replaces each word with its counterpart (again, ignoring all directives).

## Sample Usage
Just like the inspiration, assume a file called `foo.cpp` that contains the following code:

```
#include <iostream>
int main ( )  
{
	std :: cout << "mvm!" ;
	return 0 ;
}
```

Running `./mvmify foo`, we generate the file `foo_mvmified.cpp`:

```
#include  <iostream>

#define mV "mvm!"
#define mVM (
#define mVVM )
#define mVVm 0
#define mVVv ::
#define mVmm ;
#define mVv <<
#define mv cout
#define mvV main
#define mvVv return
#define mvmM std
#define mvmm {
#define mvv }

mvV mVM mVVM 
mvmm 
mvmM mVVv mv mVv mV mVmm 
mvVv mVVm mVmm 
mvv 
```
