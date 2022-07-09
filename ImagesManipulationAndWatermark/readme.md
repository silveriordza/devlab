//-----------
Version 1.0
Date: 7/9/22
Change author: Silverio Rodriguez Alcorta
Description: experimented with image-file-resize combined it with js-watermark to reduce the size of an image uploaded by a user with the "input type file" tag from HTML, the js-watermark adds a watermark in several places of the image which can be used to safeguard the copyright in case a user downloads an un-licensed image.

LESSONS LEARNED:
I modified the image-file-resize javascript code to add the watermark functionality, however I didn't used the js-watermark component since I learned form it that it is using vanilla javascript with canvas object along with context and image objects to draw the watermarks, hence I only added standard vanilla code into the image-file-resize function to add watermark when the image is being resized.

This worked well in plain vanilla HTML with script type=module tag, however when I tried to use it into a ReactJS the compilation failed with error in the line where: img.onload which is embbeded into a FileReader.onload also, perhaps React compiler don't accept this as a valid syntax, the error was:

"Expected an assignment or function call and instead saw an expression."

//-----------