# PrintOrientation-Controller

This is a FME Workbench project that adds an orientation field to a feature layer. The orientation field tells the layout engine if the feature should be printed as portrait or landscape. This project is implemented with FME 2017. 

The traditional way of doing this is to use  the script below in the field calculator/ expression interface of QGIS:

``` QGISExpression

Ratio = (x_max($geometry)-x_min($geometry))/(y_max($geometry)-y_min($geometry))
```

``` QGISExpression
PrintOrientation =
Case
when "Ratio" > 1 then 'Landscape'
when "Ratio" <= 1 then 'Portrait'
end
```

## What I Did

I have used FME to automate the process of orientation control process by calculating the ratio of the x and y axis of each layer. The result helps in determining if the layer is best presented as a Landscape or Portriat. 

With the resulting map, All you need to do as a user will be to set the orientation field in your layout/map engine to the orientation attribute of your layer.

## Contact

In case you have any questions or assitance on any thinge related, please contact mevia any of these channels.
Name: Ayodele Adeyemo
Email: christad92@gmail.com
Phone: +2348148796747
