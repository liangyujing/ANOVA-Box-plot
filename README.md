## 1. Create basic box plots:
#一个自变量一个因变量
#Use different colors for each group  边
boxplot(prejudice因 ~ suffering自, data = my_data, frame = FALSE,
        border = c("#999999", "#E69F00", "#56B4E9"))

#Change fill color : single color  填充
boxplot(len ~ dose, data = my_data, frame = FALSE,
        col = "steelblue")

#Change fill color: multiple colors  填充
boxplot(len ~ dose, data = ToothGrowth, frame = FALSE,
        col = c("#999999", "#E69F00", "#56B4E9"))

#两个自变量一个因变量
boxplot(prejudice ~ suffering*liedetection,frame = FALSE, col = c("#00AFBB", "#E7B800"),
        ylab="prejudice",
        xlab = "suffering x liedetection")

 
#表的名字
main = "Plot of length by dose",

#X Y轴的名字
xlab = "Dose (mg)", ylab = "Length",

## 2. Box plots with number of observations:
install.packages("gplots")
library("gplots")

#Box plot with annotation  显示每组的被试数
boxplot2(len ~ dose, data = ToothGrowth,
         frame = FALSE)

#Put the annotation at the top  被试数在上面
boxplot2(len ~ dose, data = ToothGrowth,
         frame = FALSE, top = TRUE)

#总之
gplots::boxplot2(len ~ dose, data = ToothGrowth,
                 frame = FALSE, top = TRUE)
