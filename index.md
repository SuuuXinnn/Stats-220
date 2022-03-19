## I used [{magick}](https://cran.r-project.org/web/packages/magick/vignettes/intro.html) package for creating the meme

```r
library(magick)

url_1 = "https://i.ytimg.com/vi/FlhHq_z6MHk/maxresdefault.jpg"
meme1 <- image_read(url_1) %>% 
  image_scale(300)

text1 <- image_blank(width = 300, height = 169, color = "#ff3333") %>%
  image_annotate(text = "Iron Man", color = "#f2f2f2", size = 40, font = "Impact", gravity = "center")

url_2 = "https://www.tjxz.cc/wp-content/uploads/2018/06/155240.jpg"
meme2<- image_read(url_2) %>% 
  image_scale(300)  

text2 <- image_blank(width = 300, height = 188, color = "#002db3") %>%
  image_annotate(text = "Captain America", color = "#f2f2f2", size = 40, font = "Impact", gravity = "center")

ironman_vector <- c(text1, meme1)
a_row <- image_append(ironman_vector)

CaptainAmerica_vector <- c(text2, meme2)
b_row <- image_append(CaptainAmerica_vector)

result <- c(a_row, b_row) %>% image_append(stack = TRUE) %>% image_scale(600)
image_write(result, "my_meme.png")
```

![](my_meme.png)


为什么要创建这个图片
创建这个图片的目的

描述图片
用了哪些元素

*hi*
**hi**








  



