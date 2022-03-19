# **Hello 😁 people who are reading my repository now**

## I used [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html) package for creating my meme photo

### These are the original photos: 
![](https://i.ytimg.com/vi/FlhHq_z6MHk/maxresdefault.jpg) 
![](http://x0.ifengimg.com/res/2019/C2D4F9E74371F0AB1B6AC13E30D876BDD34363F4_size147_w995_h806.jpeg)

### That's the photo that I create: 

![](my_meme.png)

### Here is my R code:

```r
library(magick)

url_1 = "https://i.ytimg.com/vi/FlhHq_z6MHk/maxresdefault.jpg"
meme1 <- image_read(url_1) %>% 
  image_scale(300)


text1 <- image_blank(width = 300, height = 169, color = "#e60000") %>%
  image_annotate(text = "Iron Man", color = "#f2f2f2", size = 40, font = "Impact", gravity = "center")


url_2 = "http://x0.ifengimg.com/res/2019/C2D4F9E74371F0AB1B6AC13E30D876BDD34363F4_size147_w995_h806.jpeg"
meme2<- image_read(url_2) %>% 
  image_scale(300)  


text2 <- image_blank(width = 300, height = 243, color = "#cc0000") %>%
  image_annotate(text = "Spider Man", color = "#f2f2f2", size = 40, font = "Impact", gravity = "center")

ironman_vector <- c(text1, meme1)
a_row <- image_append(ironman_vector)

SpiderMan_vector <- c(text2, meme2)
b_row <- image_append(SpiderMan_vector)

result <- c(a_row, b_row) %>% image_append(stack = TRUE) %>% image_scale(600)
image_write(result, "my_meme.png")
```
Marvel is my favourite movies, so I decided to use elements of Marvel to create my meme.




为什么要创建这个图片
创建这个图片的目的

描述图片
用了哪些元素

*hi*
**hi**








  



