## Scite
Scite is most lightweight editor and portable by nature, it is my favorite quick note and code for long time, less than 3MB.

Here is show you how to use scite as lightweight Go IDE.

## scite + go dark theme
You can download from my [github](https://github.com/robertluwang/scite-setting) and quick replaces your scite theme. Please backup your SciTEGlobal.properties if you have some change on it.

```
git clone git@github.com:robertluwang/scite-setting.git
cd scite
cp SciTEGlobal.properties <scite path>/
cp go.properties <scite path>/
```

## go.properties

Here is details for go.properties, no change needed for standard Go installation, need to change own Go path for portable Go.

```
# Define SciTE settings for Go files
# Robert Wang
# Nov 15, 2017

lexer.*.go=go
use.tabs.*.go=1
tab.size.*.go=4
indent.size.*.go=4
# copied straight from the spec, added primitive types
keywords.*.go= \
break        default      func         interface    select      \
case         defer        go           map          struct      \
chan         else         goto         package      switch      \
const        fallthrough  if           range        type        \
continue     for          import       return       var         \
bool    int     int8    int16   int32   int64                   \
byte    uint    uint8   uint16  uint32  uint64  uintptr         \
float   float32 float64 string  nil     true    false

# Keyword
style.*.5=fore:#3060A0,bold

# String
style.*.3=fore:#246161
# Single quoted string
style.*.4=fore:#246161

# command for standard Go installation on windows
command.compile.*.go=go build -i "$(FileNameExt)"
command.build.*.go=go build -i "$(FileNameExt)"
command.go.*.go=$(FileName).exe

# command sample for portable go, change to your own go path and uncomment below lines
#command.compile.*.go=C:\oldhorse\portableapps\go\bin\go build -i "$(FileNameExt)"
#command.build.*.go=C:\oldhorse\portableapps\go\bin\go build -i "$(FileNameExt)"
```
