## Introduction
ImageResize is a small PHP library for resizing any image. Size of the image can be increased or decreased by keeping the aspect ratio of the image as it is. 

## How to Use
This library is pretty simple in usage.

##### Step 1: Load the library  
`include_once("ImageResize.php");`

##### Step 2: Image to be resized  
`$input = "inputImage.png";`

##### Step 3: Output Image  
`$output = "outputImage.png";`

##### Step 4: Take the object of the library  
`$resizeObj = new ImageResize($input);`

##### Step 5: Resize the image to the dimension you want  
`$resizeObj->resize($width = 200,$height = 300);`

##### Step 6: Output the image  
`$resizeObj->output($output);`

## Example 

#### Example 1 : With Blurred image padding

`$new = new ImageResize($input);
$new->resize($width = 600, $height = 450);
$new->output($output);`

Input Image:  

![](https://s21.postimg.org/j3khle79z/nature.jpg)

Output Image:  

![](https://s15.postimg.org/e0egc11p7/nature1.jpg)


#### Example 2 : With White Space padding
`$new = new ImageResize($input);`  
`$new->options("colorpadding", true);`  
`$new->resize($width = 600, $height = 450);`  
`$new->output($output);`  

Input Image:  

![](https://s21.postimg.org/j3khle79z/nature.jpg)

Output Image:  

![](https://s22.postimg.org/axq7whz8h/nature1.jpg)

OR, if you want to put any color in the padding area

`$new = new ImageResize($input);`  
`$new->options("colorpadding", true);`  
`$new->resize($width = 600, $height = 450);`  
`$new->options("paddingcolor", array(149,213,50));`  
`$new->output($output);`  

Output Image:  

![](https://s21.postimg.org/js4ve41ef/nature1.jpg)
