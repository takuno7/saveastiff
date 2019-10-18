# saveastiff
Matlab function to save multipage TIFF images to a single file.


# Simple usage

## **function res = saveastiff(data, path, options)**

options.color: **true** or **FALSE**.
If this is true, third dimension should be 3 and the data is saved as a color image.

options.compress: **'no'**, **'lzw'**, **'jpeg'** or **'adobe'**. 'no': Uncompressed(Default). 'lzw': lossless LZW. 'jpeg': lossy JPEG (When using JPEG compression, ImageWidth, ImageLength, and RowsPerStrip must be multiples of 16.). 'adobe': lossless Adobe-style

options.jpegquality: JPEG compression qualtiy. A value **between 1.0 and 100.0**  

options.message: **TRUE** or **false**.  
If this is false, all messages are skipped.  

options.append: **true** or **FALSE** 
If path is exist, the data is appended to an existing file.  
If path is not exist, this options is ignored.  

options.overwrite: **true** or **FALSE** 
Overwrite to an existing file.  

options.big: **true** or **FALSE**
Use 64 bit addressing and allows for files > 4GB

Defalut value of 'options' is  
options.color = false;  
options.compress = 'no';  
options.message = true;  
options.append = false;  
options.overwrite = false;  
options.big = false;

res : Return value. It is 0 when the function is finished with no error.  If an error is occured in the function, it will have a positive number (error code).

## Demo
see saveastiff_demo.m file.
