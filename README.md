# modelling
https://docs.google.com/presentation/d/1Ux7t_TZtXHRowOd7E9-xMbOlQxKoVvkrADUqI-g18SM/pub?start=false&loop=false&delayms=3000&slide=id.gff2c94974_0_0

install.packages('jpeg')
library(jpeg)

img <- readJPEG('C:/Users/Administrator/Desktop/image.jpg')
h <- dim(img)[1]
w <- dim(img)[2]

img1d <- matrix(img, h*w)
str(img1d)

pca <- prcomp(img1d)
summary(pca)

image(matrix(pca$x[,1], h))  #score of pca , again to matrix
image(matrix(pca$x[,2], h), col = gray.colors())  #score of pca , again
# the 1.comp contains most of comp., but 2. contains finer differences,
# so the diff between the second and first can show the fine things...
install.packages("h2o")
library(h2o)
install.packages("hflights")
library(hflights)
#much more data use h2o

h2o.init()
# command 
java -jar "c:\Program Files\R\R-3.2.3\library\h2o\java\h2o.jar" -ip 127.0.0.1
