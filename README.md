# task8

library("magick")
library("rsvg")
tiger <- image_read_svg('http://jeroen.github.io/images/tiger.svg', width = 350)
print(tiger)
image_write(tiger, path = "Desktop/mridul.png", format = "png")
tiger_pdf <- image_convert(tiger, "pdf")
image_info(tiger_pdf)
image_write(tiger, path = "Desktop/mridul.pdf", format = "pdf")
#X11 only
image_display(tiger)
#System dependent
image_browse(tiger)
