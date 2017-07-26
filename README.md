# How-Transform-HTML-INTO-Multipage-PDF
A example about how to transform HTML into Multipage PDF.

[Preview Demo](http://pwcong.me/how-transform-html-into-multipage-pdf/)

# Support Browser
* IE10+
* Chrome
* Firefox
* 360

# Usage
## First Step.
import these js file like this:
```
        <script src="/jspdf.debug.js"></script>
        <script src="/html2canvas.js"></script>
        <script src="/renderPDF.js"></script>

```

## Last Step.
execute the method `renderPDF` that require one parameter (3 optional parameters) like this:
```
    renderPDF(document.getElementById("content"));

    // or

    renderPDF(document.getElementById("content"), "pdfName", "a4", function(){
        console.log("success");
    })

```

# API

* renderPDF(content: Element, pdfName: string, format: string, onSuccess: function )
    * content[Required]: the html element will be transfromed
    * pdfName[Optional]: the filename of PDF, default is "content"
    * format[Optional]: decide the page format of final PDF, default is "a4"
    * onSuccess[Optional]: execute the function when generate PDF successfully 

# Others
## About PDF Format

The width and height of content decided by the Format of PDF

```
    'a0': [2383.94, 3370.39], 'a1': [1683.78, 2383.94],
    'a2': [1190.55, 1683.78], 'a3': [841.89, 1190.55],
    'a4': [595.28, 841.89], 'a5': [419.53, 595.28],
    'a6': [297.64, 419.53], 'a7': [209.76, 297.64],
    'a8': [147.40, 209.76], 'a9': [104.88, 147.40],
    'a10': [73.70, 104.88], 'b0': [2834.65, 4008.19],
    'b1': [2004.09, 2834.65], 'b2': [1417.32, 2004.09],
    'b3': [1000.63, 1417.32], 'b4': [708.66, 1000.63],
    'b5': [498.90, 708.66], 'b6': [354.33, 498.90],
    'b7': [249.45, 354.33], 'b8': [175.75, 249.45],
    'b9': [124.72, 175.75], 'b10': [87.87, 124.72],
    'c0': [2599.37, 3676.54], 'c1': [1836.85, 2599.37],
    'c2': [1298.27, 1836.85], 'c3': [918.43, 1298.27],
    'c4': [649.13, 918.43], 'c5': [459.21, 649.13],
    'c6': [323.15, 459.21], 'c7': [229.61, 323.15],
    'c8': [161.57, 229.61], 'c9': [113.39, 161.57],
    'c10': [79.37, 113.39], 'dl': [311.81, 623.62],
    'letter': [612, 792],
    'government-letter': [576, 756],
    'legal': [612, 1008],
    'junior-legal': [576, 360],
    'ledger': [1224, 792],
    'tabloid': [792, 1224]
```