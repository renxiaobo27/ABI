Description About ABI_BBX.exe:


This tool is for our ABI project to identify the empty frames and bounding box in a sequence.


How to use it:

System environment : Windows

1: Put ABI_BBX.exe with all .dll files.

2: Command Parameters
	@ : Image paths file
	@ : Output path
	
The image paths file is one line by one line, such as 

		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0001.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0002.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0003.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0004.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0005.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0006.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0007.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0008.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0009.JPG
		D:\\exec\\test_seq_images\\1.10-Ocelot\\SEQ81565\\SEQ81565_IMG0010.JPG


So to run this tool, you should input the following command in windows shell:

ABI_BBX.exe $Image_File_Path $Output_Path

For example, you can run the following code for the given testing sequence:

C:\Users\YOUR_WORKING_DIR> ABI_BBX.exe F:\ABI_Deliver\imgList.txt F:\ABI_Deliver\


Output:
	A txt file named "information.txt" under your Output Path.This file is organized in JSON format:

	{ 
   		"image":  D:\exec\test_seq_images\1.02-Agouti\SEQ75520\SEQ75520_IMG0001.JPG 
   		"bbox": {
      			''xmin'': 1110 
      			''ymin'': 822 
      			''xmax'': 1386 
      			''ymax'': 1026 
   			}, 
    			"success": true
 	},
		

Tip:

	Make sure you add the frame's extension(.JPG) and please use "\\".

	
This rar file also includes one test sequence and related image path file "imgList.txt", you can change the path and then test this sequence.

If you have any questions about this tool, please email xr7rf@mail.missouri.edu
