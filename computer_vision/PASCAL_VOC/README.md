PASCAL_VOC dataset
--

# 1. dataset 구조
<pre>
<code>
- VOC2012
    - Annotations
    - ImageSets
        - Action          # class별 train, trainval, val 에 속하는 이미지 정보(33개 txt 파일)
        - Layout          # train, trainval, val에 속하는 이미지 정보 (3개 txt 파일)
        - Main            # class별 train, trainval, val 에 속하는 이미지 정보(66개 txt 파일)
        - Segmentation    # train, trainval, val에 속하는 이미지 정보   (3개 txt 파일)
    - JPEGImages
    - SegmentationClass
    - SegmentationObject
</code>
</pre>

## 1_1. Anontations 
- xml data
- JPEGImages 폴더 속 원본 image와 파일명 같음. (2007_00027.jpg, 2007_00027.xml)
- segmentation의 정답 data

    # 2007_000039.xml

    <annotation>
        <folder>VOC2012</folder>
        <filename>2007_000039.jpg</filename>
        <source>
            <database>The VOC2007 Database</database>
            <annotation>PASCAL VOC2007</annotation>
            <image>flickr</image>
        </source>
        <size>
            <width>500</width>
            <height>375</height>
            <depth>3</depth>
        </size>
        <segmented>1</segmented>
        <object>
            <name>tvmonitor</name>
            <pose>Frontal</pose>
            <truncated>0</truncated>
            <difficult>0</difficult>
            <bndbox>
                <xmin>156</xmin>
                <ymin>89</ymin>
                <xmax>344</xmax>
                <ymax>279</ymax>
            </bndbox>
        </object>
    </annotation>

## 1_2. ImageSets
- train, trainval, val 에 속하는 이미지 정보를 가짐

## 1_3. JEPGImages
- *.jpg 확장자를 가진 image file

## 1_4. SementationClass
- Segmentic Segmentation을 학습하기 위한 label 이미지

## 1.5. SeamentationObject 
- Instance Segmentation을 학습하기 위한 label 이미지




 # 2. 이미지 시각화


 |JPEGImages | SegmentationClass | SegmentationObject|
 |---|---|----|
 |<img src = "./VOCdevkit/VOC2012/JPEGImages/2007_000039.jpg" width = "200"/>|  <img src = "./VOCdevkit/VOC2012/SegmentationClass/2007_000039.png" width = "200"/>|  <img src = "./VOCdevkit/VOC2012/SegmentationObject/2007_000039.png" width = "200"/>|

 


--- 
[참고]
- [PASCAL VOC Dataset](https://deepbaksuvision.github.io/Modu_ObjectDetection/posts/02_01_PASCAL_VOC.html)
