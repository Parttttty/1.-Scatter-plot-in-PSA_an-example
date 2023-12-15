#画PSA散点图
install.packages("ggplot2")          #下载包
library("ggplot2")                   #调用包
setwd("/Users/huhansan/Documents/R")                        #设定文件夹
PSA<- read.csv("PSA 15 1 3GDP results.csv")     #读取初始文件PSA result.csv
head(PSA)
options(scipen = 1)
ggplot(PSA, aes(x=Incr.QALY,y=Incr.Cost)) +                             ##定义x,y轴
  geom_point (size = 3, shape =20, alpha = 0.35, colour = "#0383C4")+                 ##21圆形
  coord_cartesian(xlim =c(0, 0.3), ylim = c(0, 4500))+                                #设置坐标轴范围
  stat_ellipse(type = "norm", level = 0.95, size = 0.5, lty = 2, colour = "gray")+   # #设置95%置信区间#FC9D9A
  geom_abline(aes(intercept = 0, slope = 38223.34, color = "3 GDP"), lty = 5, colour = "red")+             # #设置阈值线
  geom_abline(aes(intercept = 0, slope = 12741.11, color = "1 GDP"), lty = 5, colour = "green")+             # #设置阈值线
  theme_bw()+                                                                         ###设置白色背景底色
  theme(panel.grid.major = element_blank(),
        panel.grid=element_blank(),
        legend.title =element_text())+
  labs(color = "WTP")
