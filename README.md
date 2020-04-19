# BasicR_Programs
x<-1
y<-2
z<-3
x*y*z

my_vector<-c(1,2,3,70)

x<-c(2,4,1,6,7)
y<-c(2,8,10,2,7)
x<-c(2,0,0,4)
x[1]
x[-1]
x[1]<-3;x
x[-1]=5;x
y<9
y[4]=1;y
y
y[y<9]=2;y
pnorm(740,711,29)-pnorm(697,711,29)
1-pnorm(740,711,29)

data=iris$Sepal.Length

a<-scan()

ci(a,confidence=0.95)
1-pt(1.414,49)
t
pt(0,49)
1-pt(5.89,49)
e-07
pt(5.89,49)
1-(pt(5.89,49))

t.test(x,alternative="greater",mu=0.3)

data<-read.csv("NewspaperData.csv",header=T)
data1<-data[,-1]
mymodel<-lm(sunday~daily,data=data1)
predict(mymodel,data.frame(daily=200))
summary(mymodel)

data<-read.csv("Age.csv")

mymodel2<-lm(Exp~Age,data)
predict(mymodel2,data.frame(Age=22))

summary(mymodel2)

data<-read.csv("wc-at.csv")

mymodel3<-lm(AT~Waist,data=data)
predict(mymodel3,data.frame(Waist=200))

summary(mymodel3)

cigarette_consumption<-read.csv("CigaretteConsumption(1).csv")
pairs(cigarette_consumption[,2:8])
cor(cigarette_consumption[,2:8])
reg.model<-lm(Sales~Age+HS+Income+Black+Female+Price,data=cigarette_consumption)
summary(reg.model)
dataframe<-data.frame(cigarette_consumption,"predict_values"=pred,"errors"=reg.model$residuals)
pred<-predict(reg.model)

summary(pred)

Toyota_Corolla<-read.csv("ToyotaCorolla.csv")
TC<-Toyota_Corolla[,c(3,4,7,9,13,14,16,17,18)]
pairs(TC[,2:9])
cor(TC[,2:9])
pairs(TC)
cor(TC)
model.car<-lm(Price~Age_08_04+KM+HP+cc+Doors+Gears+Quarterly_Tax+Weight,data=TC)
summary(model.car)
plot(model.car)
residualPlots(model.car,tests=F)
avPlots(model.car)
qqPlot(model.car)
influence(model.car)
infIndexPlot(model.car)
