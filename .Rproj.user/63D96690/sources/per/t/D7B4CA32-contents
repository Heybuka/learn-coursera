library(tidyverse)
ggplot(data=mpg)
ggplot(data=mpg)+geom_point(mapping=aes(x = cyl,y= hwy))
ggplot(data=mpg)+geom_point(mapping=aes(x=class, y=drv))

#class scaled with color
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy, color=class))
#class scaled with size
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy, size=class))
#class scaled with alpha
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy, alpha=class))
#class scaled with shape
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy, shape=class))
?mpg
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy), shape=25, color="red",stroke=1)
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy, color=displ<5))
?geom_point
#subplot using one variable usually for categorical data
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy))+facet_wrap(~class,nrow=2)
#subplot using two variables usually for categorical data
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy))+facet_grid(drv~cyl)
ggplot(data=mpg)+geom_point(mapping=aes(x=drv, y=cyl))
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy))+facet_grid(cyl~.)
#facet on a continous variable not advisable
ggplot(data=mpg)+geom_point(mapping=aes(x=displ, y=hwy))+facet_wrap(~cty)


#GEOMETRIC OBJECTS
ggplot(data=mpg)+
  geom_smooth(mapping=aes(x=displ, y=hwy,group=drv))
#linetype
ggplot(data=mpg)+
  geom_smooth(mapping=aes(x=displ, y=hwy,linetype=drv))
ggplot(data=mpg)+
  geom_smooth(mapping=aes(x=displ, y=hwy,color=drv), show.legend=FALSE)
#multiple geoms
ggplot(data=mpg)+
  geom_point(mapping=aes(x=displ,y=hwy))+
  geom_smooth(mapping=aes(x=displ,y=hwy))
#efficient multiple geoms
ggplot(data=mpg, mapping=aes(x=displ, y=hwy))+
       geom_point()+
       geom_smooth()
#edit local geoms
ggplot(data=mpg, mapping=aes(x=displ, y=hwy))+
  geom_point(mapping=aes(color=class))+
  geom_smooth(color="red")
?geom_smooth
ggplot(data=mpg, mapping=aes(x=displ, y=hwy))+
  geom_point(mapping=aes(color=class))+
  geom_smooth(
    data=filter(mpg, class=="subcompact"),se=FALSE
  )
ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point()+
  geom_smooth()

ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point()+
  geom_smooth(mapping=aes(group=drv))

ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point(mapping=aes(color=drv))+
  geom_smooth(mapping=aes(color=drv,group=drv))

ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point(mapping=aes(color=drv))+
  geom_smooth(mapping=aes(group=drv))

ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point(mapping=aes(color=drv))+
  geom_smooth(mapping=aes(color=drv,linetype=drv))

ggplot(data=mpg, mapping= aes(x=displ, y= hwy))+ 
  geom_point(mapping=aes(color=drv))
  
#statistical transformations
ggplot(data=diamonds)+
  geom_bar(mapping= aes(x=cut))
#stat_count as a transformation function of geom_bar
ggplot(data=diamonds)+
  stat_count(mapping=aes(x=cut))
