# Assignment 1
## Welcome to my Assignment 1 website!!!
Below is a meme I have created using Rstudio


![](spongebob_meme.png)

```
library(magick)
campus_text <- image_blank(width = 500, height = 381, color = "#3366ff") %>%
  image_annotate(text = "On campus\nlectures\n===>", color = "#ffff00", size = 80, gravity = "center")

online_text <- image_blank(width = 500, height = 375, color = "#3366ff") %>%
  image_annotate(text = "Online\nlectures\n<===", color = "#ffff00", size = 80, gravity = "center")

sb_sleep <- image_read("https://64.media.tumblr.com/d8cdf0578b1184d4d5877c60b12e2ddc/tumblr_p55fr3sc4q1vbooiso1_640.png") %>%
  image_scale(500)

sb_tired <- image_read("https://plantillasdememes.com/img/plantillas/bob-esponja-cansado11592717572.jpg") %>%
  image_scale(500)

top_row <- image_append(c(campus_text, sb_tired))
bottom_row <- image_append(c(sb_sleep, online_text))

sb_vector <- c(top_row, bottom_row)
meme_image <- image_append(sb_vector, stack = TRUE)
meme_image
```
**This meme was created with the idea of:**
1. *Viewing the top left text first*
2. *Then across to top right image*
3. *Then below to the bottom right text*
4. *And finally across to the bottom left image*

I formatted the meme to have images and text alternate so it would contrast better and look even. As a result, the viewing experience goes in a cycle rather than going left to right twice.

**Inspiration for creating the meme:**
* *Somewhat shows how I'm coping with life*
* *Relateable for a lot of students*
* *Spongebob is cool*





