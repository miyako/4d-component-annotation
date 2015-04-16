# 4d-component-annotation
SVG Annotation Editor, based on the [Label Editor](https://github.com/miyako/4d-component-label-editor) code.

![](https://github.com/miyako/4d-component-annotation/blob/master/images/1.png)

Example
---

To set the background image:

```
Editor_SET_IMAGE ("Editor";[Table_1]image)
```

To set the annotation: (XML format, compatible with the Label Editor)

```
Editor_SET_ANNOTATION ("Editor";[Table_1]annotation)
```

To retrive the annotation:

```
[Table_1]annotation:=Editor_get_annotation ("Editor")
```

To toggle the visibility of the annotation layer:

```
$event:=Form event

Case of 
 : ($event=On Load)

  Self->:=Num(Editor_Get_layer_visible ("Editor"))

 : ($event=On Clicked)

  Editor_SET_LAYER_VISIBLE ("Editor";Self->=1)

End case 
```
