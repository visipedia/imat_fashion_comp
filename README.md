# [iMaterialist Challenge on fashion at FGVC5, CVPR 2018](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018/)


![wish](imat1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/100)

As shoppers move online, it would be a dream come true to have products in photos classified automatically. But, automatic product recognition is tough because for the same product, a picture can be taken in different lighting, angles, backgrounds, and levels of occlusion. Meanwhile different fine-grained categories may look very similar, for example, royal blue vs turquoise in color. Many of today’s general-purpose recognition machines simply cannot perceive such subtle differences between photos, yet these differences could be important for shopping decisions.

Tackling issues like this is why the Conference on Computer Vision and Pattern Recognition (CVPR) has put together a workshop specifically for data scientists focused on fine-grained visual categorization called the [FGVC5 workshop](https://sites.google.com/view/fgvc5/home). As part of this workshop, CVPR is partnering with Google, Wish, and [Malong Technologies](https://www.malong.com/en/home) to challenge the data science community to help push the state of the art in automatic image classification.


## Kaggle
We used Kaggle to hold our competiton: https://www.kaggle.com/c/imaterialist-challenge-fashion-2018/


## Dataset Details

All images in the iFashion-Attribute database are provided by Wish, with 1,012,947,  9,897 and 39,706 images split into train, validation, and test sets respectively. It has 228 fine-grained fashion attribute-level classes which form
8 high-level fashion groups defined professionally from the fashion industry. Each image has multiple labels. Each group has a number of fashion classes, and the number ranges from 3 ( “gender” group) to 105 ( “category” group).


## Files

The competition data can be download on [**Google Driver**](https://drive.google.com/drive/folders/1X0Q1OPSU6QHuCuHUNVSCCxxVDSPlkQQt?usp=sharing_).

- [**train.json**](https://drive.google.com/file/d/1oh_GDZY2IQwB_eKCV1ZbWiXkVe5WGEG-/view?usp=sharing): training data with image urls and labels

- [**val.json**](https://drive.google.com/open?id=11FiOABXkkidTZbNse1zg6HnqLay_0XL5):validation data with the same format as train.json

- [**test.json**](https://drive.google.com/file/d/1E4j7z8lPrdV9uWEAADXn6UPT0dQQ81Bs/view?usp=sharing): images of which the participants need to generate predictions. Only image URLs are provided.

- [**label_map_228.xlsx**](https://drive.google.com/file/d/1n0bz2mRfAoRpGDFx2B9nl39Ige_-RSdv/view?usp=sharing): 228 attribute label map.

- **Training Data** All train/validation/test sets have the same format as shown below:

```
    {
      "images" : [image],
      "annotations" : [annotation],
    }

   image{
        "image_id" : int,
        "url": [string]
        }

   annotation{
       "image_id" : int,
       "label_id" : [int]
       }
```

Note that for each image, we only provide URLs instead of the image content. Users need to download the images by themselves. Note that the image urls are hosted by Wish so they are expected to be stable.

This year, we omit the names of the labels to avoid hand labeling the test images.

- **Testing data and submissions** The testing data only has images as shown below:

```
  {
    "images" : [image],
  }

  {
    "image_id" : int,
    "url" : [string],
  }
```


## Contact

Sheng Guo, Malong Technologies (sheng@malong.com)

Weilin Huang, Malong Technologies (whuang@malong.com)

Xiao Zhang, Google Research (andypassion@google.com)

Yin Cui, Cornell University (ycui@cs.cornell.edu)

Matt Scott, Malong Technologies (mscott@malong.com)


