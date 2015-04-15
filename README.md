# 4d-component-annotation
SVG annotation editor


```
C_LONGINT($1;$utf32)
C_TEXT($0;$char)

If (Count parameters#0)

$utf32:=$1

If ($utf32>0xFFFF)
$LEAD_OFFSET:=0xD800-(0x00010000 >> 10)
$lead:=$LEAD_OFFSET+($utf32 >> 10)
$trail:=0xDC00+($utf32 & 0x03FF)
$char:=Char($lead)+Char($trail)
Else 
$char:=Char($utf32)
End if 

End if 

$0:=$char
```
