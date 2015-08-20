# sass-named-breakpoints

Mixin for wrapping styles in predefined breakpoints. (DEPRECIATED)

<h2 style="color: orange">
Please use [sass-breakpoints](https://www.npmjs.com/package/sass-breakpoints) instead.
</h1>

## Installation

  npm install --save sass-named-breakpoints

## Usage

`cat example/example.scss`

    @import "sass-named-breakpoints";
    
    @include named_breakpoint('xs') {
      body {
        background-color: red;
      }
    }
    
    @include named_breakpoint('md') {
      body {
        background-color: green;
      }
    }
    
`sassc example/example.scss`

    @media (min-width: 0em) {
      body {
        background-color: red; }
     }
    
    @media (min-width: 48em) {
      body {
        background-color: green; }
     }
     
## Defaults
    
    $named_breakpoints: (
      "xs": 0px,    //targeting <569px devices (e.g. all iPhones <6)
      "sm": 569px,  //targeting >=569px devices (e.g. iPhones >=6)
      "md": 768px,  //targeting >=768px tablets (e.g. portrait iPad)
      "lg": 1004px  //targeting >=1024px tablets (e.g. landscape iPad) and desktops but leaving room for the scrollbar
    ) !default;

## License

The MIT License (MIT)

Copyright (c) 2014 James Newell

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.