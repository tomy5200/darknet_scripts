# darknet_scripts
This repo contains my auxilary scripts to work with darknet deep learning famework

<h2>How to reproduce YOLOv2 anchors for yolo-voc.cfg?</h2>
follow the below steps 2-5(cut from AlexeyAB's repos)

2. Download The Pascal VOC Data and unpack it to directory `build\darknet\x64\data\voc` will be created dir `build\darknet\x64\data\voc\VOCdevkit\`:
    * http://pjreddie.com/media/files/VOCtrainval_11-May-2012.tar
    * http://pjreddie.com/media/files/VOCtrainval_06-Nov-2007.tar
    * http://pjreddie.com/media/files/VOCtest_06-Nov-2007.tar
    
    2.1 Download file `voc_label.py` to dir `build\darknet\x64\data\voc`: http://pjreddie.com/media/files/voc_label.py

3. Download and install Python for Windows: https://www.python.org/ftp/python/3.5.2/python-3.5.2-amd64.exe

4. Run command: `python build\darknet\x64\data\voc\voc_label.py` (to generate files: 2007_test.txt, 2007_train.txt, 2007_val.txt, 2012_train.txt, 2012_val.txt)

5. Run command: `type 2007_train.txt 2007_val.txt 2012_*.txt > train.txt`

<h2>Is gen_anchors.py same as YOLOv2 anchor computation?</h2> 

<h4> Yes, almost. Look at the two anchors below:</h4>
<br />
<ul>

<li>
yolo-voc.cfg anchors are provided by the original author
<img src= 'https://github.com/Jumabek/darknet_scripts/blob/master/generated_anchors/voc-original/yolo-voc.png' />
</li>
<br />

<li>
yolo-voc-reproduce.cfg anchors computed by gen_anchors.py 
<img src= 'https://github.com/Jumabek/darknet_scripts/blob/master/generated_anchors/voc-anchors-reproduce/anchors5.png' />
</li>

</ul>
