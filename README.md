

```
~/ynomad# export PATH=`pwd`:$PATH
~/ynomad# echo '{"a":1,"b":2,"c":3,"d":4,"action":"go"}'  | listen 4001 | update "data.a+=15; data.c+=5" | halt "data.c>30" | reroute 4001
{"a":16,"b":2,"c":8,"d":4,"action":"go"}
{"a":31,"b":2,"c":13,"d":4,"action":"go"}
{"a":46,"b":2,"c":18,"d":4,"action":"go"}
{"a":61,"b":2,"c":23,"d":4,"action":"go"}
{"a":76,"b":2,"c":28,"d":4,"action":"go"}
{"a":91,"b":2,"c":33,"d":4,"action":"stop"}
```
