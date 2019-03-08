# AlexeyAB_darknet

Updated: Feb 20, 2019
I added this function in the source code and resolve this problem with command:

./darknet detector batch cfg/coco.data cfg/yolov3.cfg weights/yolov3.weights batch ./in_images/ ./out_images/ >./results.txt
Parameter explain:

The input images are: ./in_images/
The output images are: ./out_images/
The detection classes with percentage is saved in: ./results.txt
To reach this, you need to replace the attached detector.c into ./src/ folder and re-make the AlexeyAB darknet.

Detail process:
Install the AlexeyAB/darknet, see: github link. The darknet is installed in the folder: darknet/
Replace the darknet/src/detector.c with the detector.c:
https://github.com/vincentgong7/AlexeyAB_darknet/blob/master/detector.c
Make the project with command in darknet/ folder:
make
If you have already did the make, you may do re-make with commands:
make clean
make
You may still do for one image with:
./darknet detector test cfg/coco.data cfg/yolov3.cfg weights/yolov3.weights ./data/dog.jpg

Any questions please let me know.
vincent.gong7[at]gmail.com

Best Regards,
Vincent
