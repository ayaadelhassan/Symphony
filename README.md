# Symphony

<div align="center">

![image](https://user-images.githubusercontent.com/42722816/99877907-23fcd780-2c0a-11eb-8def-7dfbe9a26232.png)

</div>

## Project description 

The aim of this project is to develop a sheet music reader. This field is called Optical Music Recognition (OMR). Its objective is to convert sheet music to a machine-readable version. We take a simplified version where we convert an image of sheet music to a textual representation that can be further processed to produce midi files or audio files like wav or mp3. 

# project Expiation

all libraries that we use 

```
import cv2
from skimage.filters import gaussian ,threshold_otsu, threshold_local
from skimage import io
import numpy as np
```
## apply local thresholding on the image to fix the light and remove it 

```
Image_path = "note2.png"
# to read the image in a grey scale mode
Image = cv2.imread(Image_path, 0)

# handle poop lightning: by applying local thresholding on the image
# in order to apply thresholding
# calculating the block size
# ------------------------to do make it general to all images------------------------#
block_size = 41
# calculate the local threshold value
threshold_local_value  = threshold_local(Image ,block_size, offset=10)
# apply the local threshold value on the image
binary_image = Image > threshold_local_value
```

result 

![image](https://user-images.githubusercontent.com/42722816/102087446-3beb0400-3e22-11eb-83b1-e1ff83628098.png)


## Contributors
> Thanks goes to these wonderful people in the image prcessing team.
<table>
  <tr>
    <td align="center">
    <a href="https://github.com/abdallahabusedo" target="_black">
    <img src="https://avatars0.githubusercontent.com/u/42722816?s=460&u=a58d9b5480b82e1274b77f583c95d91e6982e683&v=4" width="150px;" alt="abdallah abu sedo"/>
    <br />
    <sub><b>Abdallah abu sedo</b></sub></a><a href="https://github.com/abdallahabusedo/Symphony/commits/master?author=abdallahabusedo" title="Leader">🎯</a><a href="https://github.com/abdallahabusedo/Symphony/commits/master?author=abdallahabusedo" title="Code">💻</a><a href="https://github.com/abdallahabusedo/Symphony/pulls?q=is%3Apr+author%abdallahabusedo" title="Reviewed Pull Requests">👀</a><br />
    </td>
    <td align="center"><a href="https://github.com/Areej99" target="_black"><img src="https://avatars3.githubusercontent.com/u/50124342?s=460&v=4" width="150px;" alt="Areej99"/><br /><sub><b>Areej99</b></sub></a><a href="https://github.com/abdallahabusedo/Symphony/commits/master?author=Areej99" title="Code">💻</a><br /></td>
    <td align="center"><a href="https://github.com/ayaadelhassan"  target="_black"><img src="https://avatars3.githubusercontent.com/u/50124342?s=460&v=4" width="150px;" alt="ayaadel"/><br /><sub><b>aya adel hassan</b></sub></a><a href="https://github.com/abdallahabusedo/Symphony/commits/master?author=ayaadelhassan" title="Code">💻</a><br /></td>
     <td align="center"><a href="https://github.com/ShazaMohamed"  target="_black"><img src="https://avatars3.githubusercontent.com/u/56974730?s=460&v=4" width="150px;" alt="ShazaMohamed"/><br /><sub><b>Shaza Mohamed</b></sub></a><a href="https://github.com/abdallahabusedo/Symphony/commits/master?author=ShazaMohamed" title="Code">💻</a><br /></td>
  </tr>
 </table>



finally done 
