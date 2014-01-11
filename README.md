CUED PhD Thesis Template
========================
> A PhD thesis LyX template for Cambridge University Engineering Department.

## Author(s)
*   Krishna Kumar

## License
Distributed under MIT License

## To install LyX styles:
### Linux
1. copy `PhDThesisLyX.cls` to the appropriate LaTeX folder, e.g. under linux, copy it to: `/usr/share/texmf/tex/latex`

2. run `sudo texhash` from the command line

3. copy `PhDThesisLyX.layout` to the appropriate LyX folder, e.g. under linux, copy it to: `/usr/share/lyx/layouts`

4. Reconfigure LyX by going to Tools > Reconfigure

5. Open the Thesis.lyx file, and replace the fields with your text to write your thesis.

In LyX, the `PhDThesisLyX` style should now be available as a new document class.

Make sure the University_Crest files (eps + pdf) are in the same folder as your document.


## Using the template

### Thesis Information

Go to Document > Settings > LaTeX preamble to modify the title, author, year, department fields.

### Custom Options

To set custom options supported by the class file go to Document > Settings > Document class and enter `a4paper,12pt,numbered` without quotes in the custom field.

***Paper Size***: a4paper / a5paper

`a4paper` (The University of Cambridge PhD thesis guidelines recommends a4 page size - default option) or `a5paper`: A5 Paper size is also allowed as per the Cambridge University Engineering Deparment guidelines for PhD thesis 

***FontSize***: 10pt / 11pt / 12pt

`11pt` or `12pt`(default): Font Size 10pt is NOT recommended by the University guidelines 

***Layout***: `oneside` or `twoside`(default): Printing double side (twoside) or single side.

***Mode (print / online)***: Use `print` for print version with appropriate margins and page layout. Leaving the options field blank will activate Online version. 

***index***: For index at the end of the thesis use `index`

***draft***: For draft mode without loading any images (same as draft in book) 


### Bibliography style: 

To define document class options like bibliography style (numbered / authoryear) go to Document > Settings > Document classs and enter “numbered” or “authoryear” without quotes in the custom field.

* `authoryear`: For author-year citation eg., Krishna (2013)

* `numbered`: (Default Option) For numbered and sorted citation e.g., [1,5,2]


### Choosing the Page Style

`PhDThesisLyX` defines 3 different page styles (header and footer). The following definition is for `twoside` layout.

* `default (leave empty)`: For Page Numbers in Header (Left Even, Right Odd) and Chapter Name in Header (Right Even) and Section #. Section Name (Left Odd). Blank Footer.

        Header (Even)   : 4                                                 Introduction 

        Header (Odd)    : 1.2 Section Name 		   			                5

        Footer 		    : Empty

* `PageStyleI`: For Page Numbers in Header (Left Even, Right Odd) and Chapter Name next to the Page Number on Even Side (Left Even). Section Number and Section Name and Page Number in Header on Odd Side (Right Odd). Footer is empty. Layout:

        Header (Even)   : 4 | Introduction 

        Header (Odd)    :                         			                1.2 Section Name | 5

        Footer 		    :                               Empty

* `PageStyleII`: Chapter Name on Even Side (Left Even) in Header. Section Number and Section Name in Header on Odd Side (Right Odd). Page numbering in footer. Layout:

        Header (Even)   : Introduction
        
        Header (Odd)    : 			   				                        1.2 Section Name
        
        Footer[centered]:                           	3

## Known Issues or Bugs 
* Please report to Krishna (kks32@cam.ac.uk), if you find any bugs
