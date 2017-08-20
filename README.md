# fpdf-barcode
Barcode support for FPDF
## Usage
For EAN13
```
PDF_BARCODE::EAN13(float x, float y, string barcode [, float h [, float w[, int font_size]]])
```
For UPC_A
```
PDF_BARCODE::UPC_A(float x, float y, string barcode [, float h [, float w[, int font_size]]])
```
x: abscissa of barcode.  
y: ordinate of barcode.  
barcode: value of barcode.  
h: height of barcode. Default value: 16.  
w: width of a bar. Default value: 0.35.  
font_size: font size of the text below barcode  
## Example
```
$pdf = new PDF_BARCODE('P','mm','A4');
$pdf->AddPage();
$pdf->EAN13(10,10,'012345678901', 5, 0.35, 9);
$pdf->UPC_A(10,20,'012345678901', 5, 0.35, 9);
