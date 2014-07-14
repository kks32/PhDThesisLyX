CUED PhD Thesis Template
========================
> A PhD thesis LyX template for Cambridge University Engineering Department.

## Author(s)
*   Krishna Kumar

## License
Distributed under MIT License

## To install LyX styles:

### Mac OSX

1. copy `PhDThesisLyX.cls` to the appropriate LaTeX folder, copy to: `/Users/[username]/Library/texmf/tex/latex/` or `~/Documents/`

2. run `sudo texhash` from the command line

3. copy `PhDThesisLyX.layout` to the appropriate LyX folder, `/Users/[username]/Library/Application Support/LyX-[version]/layouts/`

4. Reconfigure LyX by going to `LyX > Reconfigure`

5. Open the `Thesis.lyx` file, and replace the field with your text to write your thesis.

### Linux

1. create a local directory `mkdir -p ~/texmf/tex/latex`

2. copy `PhDThesisLyX.cls` to the appropriate LaTeX folder, e.g. under linux, copy it to: `~/texmf/tex/latex`
		`cp PhDThesisLyX.cls ~/texmf/tex/latex`

3. run `sudo texhash` from the command line

4. copy `PhDThesisLyX.layout` to the appropriate LyX folder, e.g. under linux, copy it to: `~/.lyx/layouts`.

5. Reconfigure LyX by going to Tools > Reconfigure

6. Open the `Thesis.lyx` file, and replace the fields with your text to write your thesis.

In LyX, the `PhDThesisLyX` style should now be available as a new document class.

Make sure the University_Crest files (eps + pdf) are in the same folder as your document.

### Windows OS

1. Copy `PhDThesisLyX.layout` to `C:\Users\<username>\AppData\Roaming\LyX<version>\layouts`.

2. Copy `PhDThesisLyX.cls` to `C:\Users\<username>\AppData\Roaming\MiKTeX\<version>\tex\latex` for MikTeX or `C:\texlive\texmf-local\tex\latex` for TexLive
   You may need to create this directory manually, though the parent `tex` directory should already be present.

Run `Start` -> `MikTex` -> `Settings` (or on Windows 8: `<Press Windows Key>`, Type 'settings', choose the non-admin 
   `Settings` item with MikTex icon) then click `Refresh FNDB`.

Now load Lyx and run: `Tools` -> `Reconfigure`. Once complete you'll receive a notification to restart Lyx.
Do so then load your `Thesis.lyx` and go to `Document` -> `Settings`. 
In `Document Class` (item in left sidebar list) In the `Document class` dropdown choose `PhDThesisLyX` (items are in alphabetical order).

## Using the template

### Thesis Information

Go to Document > Settings > LaTeX preamble to modify the title, author, year, department fields.

### Custom Options

To set custom options supported by the class file go to Document > Settings > Document class and enter (for example) `a4paper,12pt,numbered,oneside,draft,print` without quotes in the custom field.

***Paper Size***: a4paper / a5paper

`a4paper` (The University of Cambridge PhD thesis guidelines recommends a4 page size - default option) or `a5paper`: A5 Paper size is also allowed as per the Cambridge University Engineering Deparment guidelines for PhD thesis 

***FontSize***: 10pt / 11pt / 12pt

`11pt` or `12pt`(default): Font Size 10pt is NOT recommended by the University guidelines 

***Layout***: `oneside` or `twoside`(default): Printing double side (twoside) or single side.

***Mode (print / online)***: Use `print` for print version with appropriate margins and page layout. Leaving the options field blank will activate Online version. 

***draft***: For draft mode without loading any images (same as draft in book) 


### Bibliography style: 

To define document class options like bibliography style (numbered / authoryear) go to Document > Settings > Document classs and include `numbered` or `authoryear` without quotes in the custom field.

* `authoryear`: For author-year citation eg., Krishna (2013)

* `numbered`: (Default Option) For numbered and sorted citation e.g., [1,5,2]


### Choosing the Page Style

`PhDThesisLyX` defines 3 different page styles (header and footer). The following definition is for `twoside` layout.

Go to Document > Settings > Document class and include `PageStyleI` or `PageStyleII` in the custom field.

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

### Choosing the Fonts

`PhDThesisLyX` currently supports three fonts `Times`, `fourier` and `Latin Modern (default)`.

*   `times`: (The University of Cambridge guidelines recommend using Times). Specifying times option in the document class will use `mathptpx` or `Times` font with Math Support.
*   `fourier`: fourier font with math support
*   `default (empty)`: When no font is specified, `Latin Modern` is used as the default font with Math Support. 

Go to Document > Settings > Document class and include `times` or `fourier` in the custom field.

### Nomenclature Definition

* To sort nomenclatures in LyX you can use sort key prefix when entering a new nomenclature entry. In this case a prefix of `g` is used to denote Greek Symbols, followed by `-pi` or `-sort_key`. Use a `-` to separate sort key from the prefixes. 

The standard prefixes defined in this class are:

    * `A` or `a`: Roman Symbols

    * `G` or `g`: Greek Symbols

    * `Z` or `z`: Acronyms/Abbreviations

    * `R` or `r`: Superscripts

    * `S` or `s`: Subscripts

    * `X` or `x`: Other Symbols

### Authoryear citation (citing within parentheses)

* LyX by default doesn't support citep (Author, 2014) and only supports citet Author(2014) citation style. Possible work around is to change the order in which the citation styles are called. This works only in LyX 2.1 (or higher)

* Copy the following code to `Document>>Settings>>Local Layout`:


        CiteEngine authoryear
            Citep*[][]
            Citet*[][]
            Citealt*[][]
            Citealp*[][]
            Citeauthor*[]
            citeyear[]
            citeyearpar[][]
            nocite
        End
        
        CiteEngine numerical
            Citep*[][]
            Citet*[][]
            Citealt*[][]
            Citealp*[][]
            Citeauthor*[]
            citeyear[]
            citeyearpar[][]
            nocite
        End
    
## Known Issues or Bugs
 
*   If you find any let me know, or even better, patch it and contribute to the development of the LyX Template.

