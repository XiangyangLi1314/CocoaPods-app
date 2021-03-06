# ANSIEscapeHelper

This is an Objective-C class for dealing with ANSI escape sequences. Its main purpose is to translate between `NSString`s that contain ANSI escape sequences and similarly formatted `NSAttributedString`s.

Here's a quick and simple example of how you'd most likely want to use this class:

    AMR_ANSIEscapeHelper *ansiEscapeHelper =
        [[[AMR_ANSIEscapeHelper alloc] init] autorelease];
    
    // display an ANSI-escaped string in a text view:
    NSString *ansiEscapedStr =
        @"Let's pretend this string contains ANSI escape sequences";
    NSAttributedString *attrStr = [ansiEscapeHelper
         attributedStringWithANSIEscapedString:ansiEscapedStr];
    [[nsTextViewInstance textStorage] setAttributedString:attrStr];
    
    // get an ANSI-escaped string from a text view:
    NSAttributedString *attrStr = [nsTextViewInstance textStorage];
    NSString *ansiEscapedStr = [ansiEscapeHelper
         ansiEscapedStringWithAttributedString:attrStr];


## The MIT License

Copyright (c) Ali Rantakari

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.