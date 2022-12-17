# Instagram-Crop-Assemble

Tired of clipping your instagram screenshots by hand ? This script should help you !

Code project here : https://github.com/AphroMad/Crop-Instagram (But it's private)

## How does it work ?  

### What does it do ? 
- Trim your screenshots from Instagram 
- Put the screenshot in a image so you can use it as a phone background
- Put some screenshots in a bigger image so you can use it as a desktop / tablet wallpaper 



| Step 1 | Step 2 | Step 3 | Step 4 | 
|:---:|:---:|:---:|:---:|
| Screenshot | Croped image | Image with a background (for phone) | Group of images (for desktop / tablet) 
![step 1](https://github.com/PierreMars/Instagram-Crop-Assemble/blob/main/example/step1.png) |  ![step 2](https://github.com/PierreMars/Instagram-Crop-Assemble/blob/main/example/step2.jpg) | ![step 3](https://github.com/PierreMars/Instagram-Crop-Assemble/blob/main/example/step3.jpg) | ![step 4](https://github.com/PierreMars/Instagram-Crop-Assemble/blob/main/example/step4.png)


### How does it do that ? 
#### First thing first, crop the image (Step 1 -> Step 2)
Crop the image is the most complicated part. This part can be divided into several steps. 

- First of all, we have to find the coordinates of the recurring icons in each post (like, comments, message, settings, etc...). 
- Then, we just need to do a pixel color check to determine the upper and lower limit to the image. 
- Once the limits are found, we can crop the picture! 

![Important icons](https://github.com/PierreMars/Instagram-Crop-Assemble/blob/main/example/instaIcons.png)

#### Then, put it on a background (Step 2 -> Step 3)

Now that the images are cropped, we would like to put them all in the same format, to make phone wallpapers for example. 

- To do this, we ask the user to enter the dimensions he wants. We change the width of the image to fit the new dimensions (the height too, via a ratio). 
- Then, to avoid having an image on a white background, we calculate the average color of the pixels and put this color in the background. 
- Idea for improvement: Calculate a color gradient up / down like on instagram story. 

#### Finally, combine images (Step 3 -> Step 4)
Just as we prepared the images to use as phone wallpaper, I also coded something to have them as computer wallpaper. 

- At the beginning of this step, the user is asked for dimensions, then, by going through the list of images and their dimensions after changing size, we put the images as we go along in a large image. 

- For each final image, the first line is completed first, then the second. Then we move on to the next image, while removing the possibility of adding the images we have just used in the next wallpapers. 


