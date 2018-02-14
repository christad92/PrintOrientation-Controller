# PrintOrientation-Controller
This is a FME Workbench project that adds an orientation field to a feature layer. The orientation field tells the layout engine if the feature should be printed as portrait or landscape. This project is implemented with FME 2017. 

The traditionalway of doing this is to use  the script below in the feild calculator/ expression interface of QGIS:
```
Ratio = (x_max($geometry)-x_min($geometry))/(y_max($geometry)-y_min($geometry))
```

```
PrintOrientation = 
Case
when "Ratio" > 1 then 'Landscape'
when "Ratio" <= 1 then 'Portrait'
end
```

