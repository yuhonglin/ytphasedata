# Dataset of YouTube videos history viewcount

This folder includes the datasets used in the following research,
> *Honglin Yu, Lexing Xie and Scott Sanner, The Lifecycle of a Youtube Video: Phases, Content and Popularity, (ICWSM-15)*

## The link
  The data is hosted on [dropbox](https://www.dropbox.com/s/4af3646w8omhago/data_released.tar.bz2?dl=0).

## Source code
1. If you want to segment viewcount yourself, please find our segmentation algorithm [here](https://github.com/yuhonglin/segfit)
2. If you want to download data for your own, please look the our crawler [here](https://github.com/yuhonglin/YTCrawl)

## File Description
All files are in python's [pickle](https://docs.python.org/2/library/pickle.html) format.

### ```videoID_category.pickle```
   1. Data type : dictionary
   2. Key : videoIDs
   3. Value : category got from google API


### ```videoID_segInfo.pickle```
   1. Data type : dictionary
   2. Key : videoIDs
   3. Value : list of description of segments, following chronological order. For example, the value of video ```XXTey9OjuGc``` is ```[(0, 4, -0.373851, 2.98491, 48.4606, 1), (5, 734, 98.0916, -0.955789, 7.4257, 0)]```, this means the viewcount contains two segments. To see the parameter of each segment, please see this [readme](https://github.com/yuhonglin/segfit/blob/master/README.md) file on github.

### ```videoID_viewcount.pickle```
   1. Data type : dictionary
   2. Key : videoIDs
   3. Value : viewcount from first day of uploading. (containing 735 days)
