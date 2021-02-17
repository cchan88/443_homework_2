README
================
Chloe Chan

\#1: How many flights have a missing dep\_time? What other variables are
missing? What might these rows represent?

``` r
flights = nycflights13::flights
a <-filter(flights, is.na(flights$dep_time))
print(a)
```

    ## Time Series:
    ## Start = 1 
    ## End = 336776 
    ## Frequency = 1 
    ##            [,1]  [,2]   [,3] [,4]     [,5] [,6] [,7]     [,8] [,9] [,10]
    ##      1       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      2       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      3       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      4       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      5       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      6       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      7       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      8       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##      9       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     10       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     11       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     12       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     13       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     14       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     15       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     16       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     17       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     18       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     19       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     20       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     21       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     22       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     23       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     24       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     25       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     26       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     27       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     28       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     29       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     30       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     31       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     32       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     33       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     34       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     35       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     36       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     37       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     38       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     39       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     40       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     41       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     42       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     43       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     44       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     45       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     46       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     47       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     48       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     49       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     50       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     51       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     52       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     53       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     54       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     55       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     56       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     57       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     58       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     59       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     60       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     61       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     62       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     63       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     64       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     65       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     66       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     67       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     68       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     69       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     70       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     71       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     72       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     73       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     74       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     75       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     76       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     77       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     78       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     79       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     80       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     81       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     82       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     83       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     84       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     85       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     86       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     87       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     88       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     89       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     90       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     91       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     92       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     93       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     94       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     95       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     96       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     97       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     98       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##     99       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    264       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    265       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    266       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    267       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    268       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    269       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    270       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    271       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    272       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    273       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    274       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    275       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    276       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    277       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    278       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    279       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    280       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    281       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    282       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    283       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    284       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    285       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    286       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    287       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    288       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    289       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    290       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    291       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    292       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    293       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    294       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    295       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    296       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    297       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    298       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    299       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    300       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    301       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    302       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    303       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    304       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    305       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    306       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    307       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    308       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    309       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    310       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    311       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    312       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    313       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    314       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    315       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    316       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    317       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    318       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    319       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    320       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    321       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    322       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    323       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    324       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    325       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    326       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    327       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    328       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    329       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    330       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    331       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    332       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    333       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    334       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    335       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    336       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    337       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    338       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    339       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    340       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    341       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    342       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    343       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    344       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    345       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    346       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    347       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    348       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    349       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    350       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    351       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    352       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    353       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    354       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    355       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    356       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    357       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    358       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    359       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    360       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    361       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    362       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    363       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    364       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    365       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    366       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    367       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    368       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    369       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    370       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    371       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    372       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    373       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    374       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    375       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    376       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    377       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    378       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    379       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    380       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    381       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    382       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    383       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    384       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    385       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    386       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    387       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    388       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    389       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    390       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    391       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    392       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    393       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    394       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    395       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    396       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    397       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    398       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    399       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    400       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    401       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    402       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    403       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    404       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    405       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    406       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    407       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    408       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    409       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    410       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    411       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    412       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    413       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    414       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    415       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    416       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    417       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    418       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    419       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    420       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    421       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    422       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    423       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    424       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    425       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    426       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    427       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    428       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    429       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    430       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    431       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    432       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    433       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    434       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    435       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    436       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    437       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    438       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    439       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    440       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    441       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    442       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    443       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    444       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    445       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    446       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    447       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    448       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    449       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    450       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    451       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    452       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    453       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    454       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    455       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    456       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    457       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    458       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    459       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    460       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    461       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    462       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    463       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    464       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    465       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    466       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    467       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    468       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    469       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    470       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    471       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    472       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    473       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    474       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    475       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    476       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    477       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    478       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    479       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    480       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    481       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    482       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    483       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    484       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    485       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    486       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    487       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    488       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    489       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    490       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    491       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    492       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    493       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    494       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    495       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    496       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    497       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    498       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    499       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    500       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    501       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    502       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    503       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    504       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    505       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    506       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    507       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    508       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    509       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    510       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    511       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    512       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    513       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    514       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    515       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    516       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    517       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    518       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    519       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    520       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    521       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    522       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    523       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    524       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    525       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    526       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    527       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    528       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    529       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    530       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    531       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    532       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    533       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    534       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    535       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    536       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    537       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    538       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    539       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    540       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    541       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    542       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    543       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    544       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    545       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    546       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    547       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    548       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    549       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    550       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    551       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    552       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    553       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    554       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    555       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    556       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    557       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    558       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    559       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    560       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    561       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    562       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    563       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    564       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    565       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    566       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    567       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    568       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    569       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    570       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    571       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    572       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    573       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    574       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    575       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    576       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    577       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    578       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    579       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    580       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    581       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    582       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    583       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    584       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    585       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    586       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    587       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    588       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    589       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    590       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    591       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    592       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    593       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    594       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    595       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    596       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    597       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    598       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    599       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    600       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    601       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    602       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    603       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    604       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    605       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    606       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    607       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    608       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    609       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    610       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    611       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    612       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    613       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    614       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    615       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    616       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    617       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    618       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    619       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    620       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    621       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    622       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    623       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    624       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    625       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    626       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    627       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    628       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    629       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    630       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    631       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    632       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    633       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    634       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    635       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    636       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    637       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    638       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    639       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    640       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    641       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    642       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    643       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    644       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    645       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    646       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    647       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    648       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    649       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    650       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    651       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    652       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    653       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    654       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    655       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    656       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    657       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    658       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    659       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    660       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    661       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    662       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    663       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    664       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    665       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    666       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    667       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    668       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    669       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    670       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    671       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    672       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    673       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    674       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    675       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    676       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    677       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    678       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    679       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    680       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    681       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    682       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    683       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    684       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    685       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    686       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    687       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    688       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    689       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    690       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    691       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    692       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    693       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    694       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    695       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    696       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    697       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    698       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    699       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    700       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    701       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    702       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    703       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    704       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    705       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    706       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    707       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    708       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    709       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    710       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    711       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    712       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    713       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    714       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    715       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    716       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    717       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    718       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    719       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    720       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    721       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    722       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    723       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    724       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    725       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    726       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    727       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    728       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    729       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    730       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    731       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    732       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    733       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    734       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    735       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    736       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    737       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    738       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    739       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    740       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    741       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    742       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    743       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    744       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    745       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    746       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    747       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    748       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    749       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    750       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    751       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    752       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    753       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    754       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    755       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    756       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    757       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    758       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    759       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    760       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    761       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    762       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    763       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    764       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    765       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    766       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    767       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    768       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    769       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    770       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    771       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    772       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    773       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    774       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    775       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    776       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    777       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    778       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    779       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    780       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    781       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    782       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    783       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    784       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    785       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    786       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    787       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    788       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    789       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    790       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    791       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    792       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    793       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    794       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    795       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    796       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    797       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    798       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    799       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    800       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    801       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    802       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    803       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    804       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    805       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    806       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    807       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    808       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    809       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    810       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    811       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    812       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    813       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    814       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    815       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    816       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    817       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    818       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    819       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    820       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    821       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    822       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    823       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    824       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    825       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    826       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    827       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    828       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    829       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    830       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    831       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    832       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    833       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    834       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    835       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    836       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    837       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    838       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    839       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    840       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    841       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    842       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    843       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    844       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    845       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    846       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    847       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    848       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    849       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    850       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    851       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    852       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    853       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    854       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    855       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    856       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    857       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    858       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    859       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    860       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    861       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    862       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    863       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    864       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    865       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    866       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    867       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    868       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    869       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    870       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    871       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    872       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    873       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    874       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    875       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    876       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    877       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    878       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    879       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    880       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    881       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    882       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    883       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    884       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    885       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    886       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    887       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    888       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    889       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    890       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    891       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    892       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    893       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    894       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    895       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    896       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    897       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    898       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    899       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    900       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    901       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    902       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    903       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    904       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    905       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    906       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    907       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    908       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    909       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    910       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    911       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    912       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    913       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    914       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    915       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    916       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    917       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    918       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    919       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    920       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    921       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    922       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    923       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    924       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    925       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    926       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    927       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    928       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    929       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    930       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    931       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    932       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    933       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    934       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    935       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    936       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    937       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    938       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    939       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    940       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    941       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    942       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    943       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    944       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    945       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    946       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    947       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    948       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    949       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    950       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    951       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    952       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    953       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    954       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    955       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    956       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    957       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    958       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    959       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    960       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    961       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    962       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    963       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    964       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    965       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    966       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    967       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    968       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    969       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    970       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    971       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    972       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    973       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    974       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    975       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    976       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    977       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    978       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    979       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    980       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    981       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    982       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    983       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    984       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    985       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    986       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    987       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    988       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    989       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    990       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    991       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    992       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    993       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    994       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    995       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    996       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    997       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    998       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##    999       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1000       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1001       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1002       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1003       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1004       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1005       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1006       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1007       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1008       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1009       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1010       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1011       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1012       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1013       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1014       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1015       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1016       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1017       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1018       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1019       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1020       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1021       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1022       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1023       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1024       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1025       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1026       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1027       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1028       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1029       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1030       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1031       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1032       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1033       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1034       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1035       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1036       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1037       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1038       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1039       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1040       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1041       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1042       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1043       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1044       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1045       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1046       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1047       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1048       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1049       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1050       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1051       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1052       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1053       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1054       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1055       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1056       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1057       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1058       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1059       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1060       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1061       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1062       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1063       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1064       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1065       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1066       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1067       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1068       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1069       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1070       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1071       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1072       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1073       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1074       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1075       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1076       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1077       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1078       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1079       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1080       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1081       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1082       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1083       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1084       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1085       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1086       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1087       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1088       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1089       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1090       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1091       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1092       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1093       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1094       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1095       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1096       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1097       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1098       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1099       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1264       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1265       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1266       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1267       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1268       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1269       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1270       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1271       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1272       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1273       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1274       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1275       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1276       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1277       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1278       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1279       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1280       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1281       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1282       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1283       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1284       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1285       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1286       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1287       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1288       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1289       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1290       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1291       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1292       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1293       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1294       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1295       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1296       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1297       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1298       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1299       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1300       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1301       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1302       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1303       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1304       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1305       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1306       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1307       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1308       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1309       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1310       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1311       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1312       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1313       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1314       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1315       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1316       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1317       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1318       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1319       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1320       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1321       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1322       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1323       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1324       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1325       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1326       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1327       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1328       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1329       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1330       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1331       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1332       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1333       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1334       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1335       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1336       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1337       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1338       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1339       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1340       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1341       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1342       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1343       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1344       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1345       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1346       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1347       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1348       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1349       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1350       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1351       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1352       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1353       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1354       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1355       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1356       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1357       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1358       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1359       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1360       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1361       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1362       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1363       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1364       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1365       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1366       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1367       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1368       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1369       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1370       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1371       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1372       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1373       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1374       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1375       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1376       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1377       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1378       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1379       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1380       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1381       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1382       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1383       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1384       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1385       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1386       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1387       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1388       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1389       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1390       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1391       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1392       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1393       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1394       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1395       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1396       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1397       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1398       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1399       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1400       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1401       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1402       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1403       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1404       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1405       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1406       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1407       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1408       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1409       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1410       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1411       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1412       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1413       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1414       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1415       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1416       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1417       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1418       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1419       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1420       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1421       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1422       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1423       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1424       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1425       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1426       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1427       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1428       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1429       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1430       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1431       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1432       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1433       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1434       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1435       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1436       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1437       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1438       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1439       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1440       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1441       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1442       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1443       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1444       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1445       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1446       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1447       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1448       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1449       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1450       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1451       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1452       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1453       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1454       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1455       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1456       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1457       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1458       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1459       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1460       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1461       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1462       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1463       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1464       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1465       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1466       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1467       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1468       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1469       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1470       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1471       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1472       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1473       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1474       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1475       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1476       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1477       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1478       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1479       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1480       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1481       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1482       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1483       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1484       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1485       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1486       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1487       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1488       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1489       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1490       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1491       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1492       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1493       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1494       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1495       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1496       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1497       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1498       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1499       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1500       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1501       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1502       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1503       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1504       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1505       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1506       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1507       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1508       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1509       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1510       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1511       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1512       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1513       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1514       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1515       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1516       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1517       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1518       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1519       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1520       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1521       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1522       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1523       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1524       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1525       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1526       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1527       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1528       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1529       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1530       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1531       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1532       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1533       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1534       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1535       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1536       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1537       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1538       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1539       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1540       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1541       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1542       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1543       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1544       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1545       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1546       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1547       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1548       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1549       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1550       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1551       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1552       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1553       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1554       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1555       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1556       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1557       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1558       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1559       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1560       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1561       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1562       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1563       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1564       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1565       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1566       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1567       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1568       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1569       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1570       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1571       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1572       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1573       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1574       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1575       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1576       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1577       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1578       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1579       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1580       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1581       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1582       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1583       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1584       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1585       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1586       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1587       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1588       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1589       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1590       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1591       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1592       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1593       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1594       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1595       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1596       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1597       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1598       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1599       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1600       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1601       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1602       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1603       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1604       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1605       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1606       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1607       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1608       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1609       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1610       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1611       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1612       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1613       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1614       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1615       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1616       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1617       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1618       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1619       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1620       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1621       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1622       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1623       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1624       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1625       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1626       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1627       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1628       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1629       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1630       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1631       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1632       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1633       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1634       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1635       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1636       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1637       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1638       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1639       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1640       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1641       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1642       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1643       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1644       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1645       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1646       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1647       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1648       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1649       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1650       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1651       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1652       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1653       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1654       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1655       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1656       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1657       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1658       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1659       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1660       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1661       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1662       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1663       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1664       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1665       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1666       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1667       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1668       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1669       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1670       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1671       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1672       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1673       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1674       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1675       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1676       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1677       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1678       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1679       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1680       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1681       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1682       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1683       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1684       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1685       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1686       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1687       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1688       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1689       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1690       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1691       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1692       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1693       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1694       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1695       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1696       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1697       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1698       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1699       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1700       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1701       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1702       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1703       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1704       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1705       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1706       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1707       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1708       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1709       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1710       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1711       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1712       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1713       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1714       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1715       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1716       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1717       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1718       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1719       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1720       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1721       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1722       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1723       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1724       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1725       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1726       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1727       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1728       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1729       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1730       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1731       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1732       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1733       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1734       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1735       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1736       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1737       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1738       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1739       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1740       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1741       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1742       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1743       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1744       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1745       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1746       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1747       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1748       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1749       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1750       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1751       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1752       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1753       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1754       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1755       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1756       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1757       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1758       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1759       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1760       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1761       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1762       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1763       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1764       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1765       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1766       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1767       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1768       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1769       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1770       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1771       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1772       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1773       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1774       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1775       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1776       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1777       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1778       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1779       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1780       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1781       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1782       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1783       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1784       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1785       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1786       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1787       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1788       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1789       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1790       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1791       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1792       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1793       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1794       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1795       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1796       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1797       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1798       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1799       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1800       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1801       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1802       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1803       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1804       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1805       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1806       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1807       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1808       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1809       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1810       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1811       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1812       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1813       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1814       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1815       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1816       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1817       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1818       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1819       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1820       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1821       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1822       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1823       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1824       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1825       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1826       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1827       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1828       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1829       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1830       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1831       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1832       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1833       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1834       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1835       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1836       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1837       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1838       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1839       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1840       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1841       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1842       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1843       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1844       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1845       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1846       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1847       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1848       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1849       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1850       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1851       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1852       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1853       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1854       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1855       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1856       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1857       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1858       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1859       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1860       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1861       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1862       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1863       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1864       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1865       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1866       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1867       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1868       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1869       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1870       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1871       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1872       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1873       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1874       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1875       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1876       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1877       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1878       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1879       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1880       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1881       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1882       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1883       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1884       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1885       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1886       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1887       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1888       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1889       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1890       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1891       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1892       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1893       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1894       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1895       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1896       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1897       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1898       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1899       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1900       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1901       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1902       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1903       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1904       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1905       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1906       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1907       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1908       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1909       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1910       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1911       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1912       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1913       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1914       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1915       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1916       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1917       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1918       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1919       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1920       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1921       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1922       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1923       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1924       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1925       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1926       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1927       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1928       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1929       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1930       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1931       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1932       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1933       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1934       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1935       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1936       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1937       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1938       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1939       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1940       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1941       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1942       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1943       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1944       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1945       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1946       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1947       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1948       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1949       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1950       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1951       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1952       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1953       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1954       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1955       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1956       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1957       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1958       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1959       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1960       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1961       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1962       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1963       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1964       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1965       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1966       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1967       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1968       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1969       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1970       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1971       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1972       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1973       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1974       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1975       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1976       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1977       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1978       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1979       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1980       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1981       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1982       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1983       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1984       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1985       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1986       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1987       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1988       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1989       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1990       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1991       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1992       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1993       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1994       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1995       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1996       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1997       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1998       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   1999       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2000       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2001       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2002       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2003       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2004       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2005       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2006       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2007       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2008       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2009       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2010       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2011       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2012       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2013       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2014       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2015       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2016       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2017       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2018       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2019       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2020       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2021       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2022       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2023       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2024       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2025       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2026       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2027       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2028       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2029       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2030       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2031       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2032       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2033       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2034       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2035       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2036       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2037       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2038       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2039       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2040       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2041       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2042       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2043       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2044       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2045       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2046       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2047       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2048       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2049       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2050       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2051       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2052       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2053       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2054       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2055       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2056       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2057       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2058       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2059       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2060       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2061       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2062       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2063       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2064       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2065       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2066       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2067       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2068       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2069       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2070       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2071       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2072       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2073       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2074       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2075       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2076       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2077       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2078       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2079       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2080       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2081       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2082       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2083       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2084       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2085       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2086       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2087       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2088       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2089       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2090       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2091       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2092       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2093       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2094       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2095       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2096       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2097       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2098       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2099       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2264       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2265       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2266       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2267       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2268       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2269       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2270       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2271       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2272       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2273       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2274       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2275       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2276       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2277       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2278       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2279       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2280       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2281       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2282       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2283       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2284       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2285       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2286       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2287       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2288       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2289       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2290       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2291       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2292       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2293       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2294       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2295       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2296       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2297       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2298       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2299       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2300       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2301       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2302       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2303       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2304       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2305       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2306       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2307       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2308       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2309       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2310       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2311       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2312       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2313       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2314       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2315       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2316       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2317       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2318       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2319       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2320       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2321       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2322       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2323       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2324       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2325       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2326       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2327       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2328       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2329       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2330       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2331       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2332       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2333       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2334       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2335       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2336       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2337       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2338       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2339       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2340       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2341       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2342       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2343       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2344       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2345       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2346       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2347       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2348       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2349       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2350       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2351       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2352       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2353       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2354       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2355       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2356       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2357       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2358       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2359       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2360       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2361       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2362       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2363       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2364       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2365       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2366       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2367       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2368       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2369       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2370       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2371       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2372       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2373       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2374       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2375       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2376       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2377       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2378       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2379       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2380       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2381       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2382       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2383       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2384       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2385       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2386       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2387       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2388       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2389       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2390       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2391       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2392       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2393       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2394       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2395       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2396       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2397       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2398       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2399       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2400       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2401       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2402       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2403       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2404       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2405       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2406       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2407       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2408       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2409       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2410       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2411       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2412       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2413       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2414       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2415       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2416       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2417       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2418       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2419       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2420       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2421       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2422       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2423       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2424       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2425       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2426       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2427       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2428       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2429       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2430       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2431       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2432       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2433       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2434       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2435       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2436       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2437       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2438       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2439       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2440       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2441       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2442       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2443       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2444       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2445       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2446       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2447       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2448       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2449       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2450       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2451       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2452       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2453       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2454       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2455       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2456       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2457       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2458       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2459       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2460       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2461       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2462       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2463       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2464       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2465       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2466       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2467       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2468       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2469       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2470       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2471       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2472       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2473       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2474       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2475       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2476       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2477       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2478       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2479       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2480       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2481       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2482       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2483       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2484       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2485       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2486       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2487       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2488       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2489       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2490       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2491       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2492       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2493       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2494       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2495       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2496       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2497       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2498       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2499       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2500       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2501       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2502       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2503       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2504       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2505       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2506       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2507       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2508       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2509       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2510       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2511       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2512       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2513       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2514       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2515       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2516       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2517       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2518       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2519       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2520       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2521       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2522       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2523       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2524       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2525       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2526       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2527       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2528       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2529       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2530       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2531       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2532       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2533       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2534       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2535       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2536       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2537       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2538       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2539       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2540       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2541       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2542       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2543       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2544       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2545       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2546       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2547       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2548       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2549       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2550       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2551       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2552       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2553       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2554       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2555       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2556       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2557       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2558       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2559       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2560       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2561       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2562       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2563       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2564       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2565       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2566       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2567       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2568       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2569       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2570       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2571       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2572       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2573       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2574       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2575       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2576       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2577       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2578       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2579       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2580       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2581       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2582       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2583       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2584       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2585       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2586       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2587       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2588       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2589       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2590       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2591       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2592       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2593       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2594       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2595       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2596       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2597       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2598       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2599       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2600       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2601       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2602       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2603       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2604       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2605       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2606       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2607       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2608       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2609       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2610       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2611       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2612       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2613       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2614       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2615       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2616       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2617       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2618       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2619       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2620       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2621       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2622       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2623       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2624       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2625       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2626       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2627       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2628       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2629       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2630       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2631       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2632       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2633       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2634       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2635       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2636       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2637       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2638       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2639       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2640       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2641       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2642       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2643       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2644       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2645       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2646       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2647       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2648       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2649       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2650       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2651       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2652       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2653       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2654       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2655       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2656       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2657       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2658       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2659       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2660       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2661       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2662       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2663       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2664       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2665       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2666       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2667       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2668       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2669       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2670       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2671       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2672       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2673       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2674       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2675       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2676       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2677       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2678       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2679       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2680       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2681       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2682       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2683       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2684       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2685       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2686       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2687       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2688       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2689       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2690       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2691       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2692       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2693       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2694       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2695       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2696       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2697       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2698       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2699       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2700       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2701       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2702       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2703       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2704       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2705       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2706       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2707       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2708       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2709       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2710       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2711       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2712       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2713       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2714       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2715       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2716       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2717       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2718       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2719       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2720       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2721       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2722       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2723       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2724       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2725       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2726       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2727       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2728       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2729       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2730       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2731       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2732       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2733       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2734       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2735       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2736       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2737       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2738       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2739       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2740       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2741       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2742       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2743       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2744       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2745       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2746       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2747       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2748       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2749       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2750       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2751       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2752       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2753       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2754       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2755       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2756       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2757       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2758       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2759       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2760       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2761       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2762       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2763       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2764       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2765       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2766       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2767       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2768       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2769       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2770       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2771       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2772       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2773       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2774       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2775       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2776       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2777       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2778       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2779       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2780       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2781       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2782       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2783       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2784       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2785       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2786       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2787       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2788       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2789       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2790       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2791       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2792       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2793       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2794       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2795       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2796       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2797       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2798       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2799       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2800       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2801       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2802       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2803       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2804       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2805       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2806       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2807       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2808       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2809       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2810       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2811       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2812       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2813       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2814       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2815       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2816       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2817       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2818       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2819       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2820       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2821       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2822       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2823       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2824       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2825       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2826       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2827       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2828       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2829       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2830       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2831       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2832       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2833       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2834       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2835       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2836       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2837       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2838       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2839       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2840       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2841       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2842       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2843       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2844       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2845       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2846       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2847       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2848       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2849       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2850       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2851       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2852       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2853       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2854       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2855       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2856       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2857       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2858       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2859       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2860       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2861       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2862       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2863       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2864       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2865       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2866       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2867       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2868       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2869       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2870       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2871       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2872       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2873       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2874       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2875       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2876       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2877       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2878       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2879       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2880       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2881       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2882       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2883       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2884       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2885       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2886       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2887       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2888       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2889       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2890       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2891       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2892       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2893       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2894       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2895       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2896       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2897       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2898       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2899       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2900       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2901       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2902       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2903       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2904       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2905       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2906       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2907       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2908       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2909       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2910       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2911       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2912       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2913       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2914       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2915       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2916       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2917       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2918       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2919       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2920       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2921       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2922       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2923       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2924       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2925       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2926       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2927       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2928       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2929       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2930       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2931       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2932       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2933       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2934       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2935       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2936       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2937       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2938       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2939       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2940       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2941       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2942       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2943       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2944       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2945       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2946       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2947       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2948       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2949       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2950       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2951       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2952       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2953       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2954       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2955       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2956       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2957       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2958       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2959       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2960       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2961       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2962       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2963       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2964       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2965       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2966       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2967       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2968       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2969       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2970       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2971       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2972       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2973       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2974       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2975       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2976       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2977       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2978       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2979       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2980       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2981       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2982       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2983       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2984       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2985       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2986       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2987       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2988       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2989       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2990       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2991       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2992       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2993       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2994       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2995       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2996       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2997       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2998       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   2999       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3000       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3001       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3002       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3003       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3004       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3005       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3006       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3007       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3008       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3009       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3010       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3011       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3012       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3013       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3014       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3015       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3016       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3017       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3018       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3019       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3020       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3021       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3022       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3023       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3024       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3025       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3026       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3027       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3028       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3029       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3030       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3031       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3032       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3033       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3034       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3035       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3036       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3037       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3038       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3039       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3040       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3041       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3042       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3043       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3044       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3045       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3046       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3047       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3048       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3049       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3050       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3051       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3052       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3053       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3054       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3055       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3056       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3057       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3058       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3059       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3060       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3061       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3062       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3063       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3064       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3065       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3066       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3067       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3068       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3069       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3070       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3071       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3072       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3073       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3074       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3075       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3076       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3077       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3078       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3079       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3080       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3081       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3082       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3083       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3084       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3085       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3086       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3087       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3088       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3089       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3090       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3091       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3092       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3093       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3094       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3095       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3096       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3097       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3098       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3099       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3264       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3265       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3266       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3267       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3268       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3269       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3270       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3271       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3272       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3273       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3274       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3275       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3276       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3277       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3278       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3279       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3280       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3281       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3282       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3283       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3284       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3285       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3286       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3287       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3288       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3289       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3290       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3291       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3292       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3293       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3294       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3295       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3296       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3297       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3298       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3299       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3300       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3301       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3302       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3303       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3304       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3305       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3306       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3307       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3308       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3309       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3310       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3311       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3312       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3313       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3314       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3315       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3316       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3317       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3318       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3319       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3320       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3321       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3322       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3323       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3324       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3325       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3326       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3327       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3328       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3329       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3330       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3331       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3332       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3333       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3334       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3335       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3336       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3337       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3338       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3339       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3340       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3341       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3342       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3343       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3344       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3345       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3346       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3347       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3348       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3349       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3350       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3351       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3352       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3353       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3354       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3355       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3356       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3357       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3358       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3359       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3360       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3361       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3362       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3363       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3364       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3365       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3366       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3367       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3368       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3369       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3370       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3371       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3372       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3373       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3374       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3375       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3376       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3377       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3378       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3379       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3380       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3381       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3382       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3383       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3384       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3385       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3386       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3387       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3388       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3389       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3390       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3391       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3392       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3393       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3394       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3395       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3396       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3397       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3398       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3399       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3400       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3401       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3402       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3403       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3404       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3405       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3406       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3407       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3408       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3409       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3410       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3411       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3412       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3413       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3414       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3415       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3416       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3417       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3418       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3419       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3420       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3421       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3422       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3423       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3424       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3425       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3426       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3427       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3428       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3429       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3430       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3431       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3432       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3433       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3434       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3435       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3436       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3437       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3438       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3439       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3440       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3441       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3442       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3443       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3444       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3445       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3446       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3447       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3448       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3449       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3450       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3451       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3452       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3453       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3454       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3455       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3456       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3457       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3458       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3459       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3460       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3461       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3462       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3463       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3464       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3465       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3466       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3467       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3468       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3469       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3470       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3471       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3472       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3473       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3474       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3475       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3476       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3477       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3478       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3479       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3480       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3481       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3482       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3483       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3484       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3485       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3486       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3487       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3488       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3489       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3490       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3491       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3492       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3493       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3494       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3495       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3496       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3497       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3498       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3499       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3500       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3501       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3502       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3503       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3504       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3505       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3506       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3507       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3508       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3509       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3510       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3511       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3512       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3513       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3514       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3515       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3516       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3517       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3518       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3519       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3520       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3521       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3522       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3523       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3524       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3525       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3526       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3527       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3528       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3529       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3530       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3531       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3532       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3533       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3534       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3535       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3536       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3537       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3538       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3539       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3540       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3541       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3542       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3543       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3544       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3545       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3546       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3547       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3548       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3549       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3550       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3551       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3552       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3553       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3554       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3555       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3556       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3557       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3558       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3559       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3560       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3561       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3562       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3563       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3564       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3565       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3566       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3567       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3568       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3569       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3570       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3571       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3572       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3573       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3574       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3575       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3576       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3577       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3578       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3579       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3580       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3581       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3582       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3583       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3584       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3585       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3586       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3587       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3588       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3589       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3590       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3591       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3592       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3593       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3594       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3595       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3596       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3597       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3598       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3599       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3600       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3601       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3602       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3603       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3604       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3605       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3606       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3607       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3608       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3609       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3610       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3611       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3612       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3613       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3614       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3615       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3616       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3617       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3618       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3619       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3620       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3621       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3622       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3623       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3624       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3625       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3626       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3627       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3628       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3629       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3630       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3631       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3632       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3633       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3634       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3635       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3636       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3637       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3638       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3639       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3640       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3641       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3642       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3643       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3644       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3645       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3646       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3647       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3648       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3649       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3650       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3651       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3652       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3653       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3654       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3655       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3656       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3657       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3658       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3659       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3660       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3661       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3662       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3663       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3664       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3665       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3666       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3667       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3668       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3669       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3670       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3671       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3672       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3673       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3674       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3675       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3676       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3677       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3678       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3679       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3680       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3681       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3682       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3683       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3684       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3685       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3686       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3687       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3688       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3689       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3690       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3691       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3692       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3693       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3694       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3695       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3696       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3697       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3698       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3699       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3700       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3701       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3702       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3703       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3704       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3705       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3706       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3707       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3708       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3709       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3710       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3711       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3712       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3713       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3714       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3715       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3716       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3717       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3718       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3719       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3720       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3721       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3722       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3723       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3724       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3725       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3726       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3727       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3728       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3729       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3730       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3731       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3732       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3733       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3734       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3735       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3736       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3737       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3738       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3739       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3740       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3741       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3742       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3743       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3744       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3745       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3746       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3747       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3748       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3749       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3750       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3751       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3752       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3753       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3754       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3755       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3756       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3757       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3758       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3759       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3760       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3761       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3762       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3763       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3764       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3765       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3766       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3767       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3768       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3769       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3770       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3771       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3772       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3773       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3774       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3775       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3776       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3777       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3778       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3779       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3780       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3781       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3782       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3783       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3784       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3785       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3786       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3787       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3788       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3789       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3790       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3791       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3792       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3793       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3794       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3795       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3796       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3797       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3798       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3799       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3800       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3801       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3802       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3803       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3804       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3805       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3806       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3807       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3808       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3809       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3810       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3811       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3812       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3813       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3814       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3815       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3816       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3817       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3818       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3819       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3820       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3821       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3822       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3823       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3824       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3825       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3826       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3827       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3828       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3829       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3830       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3831       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3832       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3833       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3834       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3835       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3836       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3837       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3838       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3839       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3840       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3841       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3842       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3843       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3844       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3845       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3846       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3847       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3848       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3849       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3850       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3851       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3852       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3853       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3854       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3855       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3856       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3857       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3858       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3859       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3860       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3861       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3862       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3863       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3864       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3865       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3866       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3867       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3868       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3869       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3870       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3871       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3872       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3873       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3874       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3875       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3876       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3877       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3878       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3879       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3880       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3881       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3882       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3883       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3884       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3885       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3886       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3887       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3888       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3889       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3890       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3891       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3892       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3893       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3894       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3895       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3896       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3897       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3898       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3899       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3900       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3901       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3902       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3903       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3904       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3905       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3906       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3907       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3908       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3909       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3910       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3911       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3912       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3913       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3914       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3915       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3916       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3917       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3918       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3919       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3920       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3921       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3922       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3923       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3924       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3925       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3926       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3927       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3928       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3929       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3930       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3931       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3932       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3933       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3934       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3935       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3936       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3937       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3938       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3939       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3940       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3941       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3942       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3943       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3944       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3945       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3946       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3947       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3948       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3949       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3950       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3951       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3952       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3953       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3954       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3955       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3956       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3957       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3958       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3959       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3960       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3961       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3962       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3963       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3964       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3965       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3966       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3967       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3968       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3969       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3970       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3971       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3972       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3973       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3974       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3975       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3976       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3977       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3978       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3979       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3980       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3981       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3982       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3983       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3984       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3985       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3986       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3987       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3988       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3989       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3990       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3991       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3992       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3993       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3994       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3995       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3996       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3997       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3998       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   3999       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4000       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4001       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4002       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4003       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4004       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4005       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4006       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4007       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4008       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4009       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4010       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4011       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4012       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4013       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4014       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4015       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4016       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4017       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4018       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4019       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4020       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4021       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4022       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4023       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4024       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4025       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4026       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4027       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4028       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4029       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4030       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4031       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4032       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4033       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4034       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4035       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4036       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4037       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4038       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4039       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4040       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4041       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4042       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4043       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4044       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4045       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4046       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4047       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4048       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4049       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4050       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4051       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4052       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4053       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4054       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4055       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4056       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4057       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4058       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4059       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4060       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4061       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4062       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4063       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4064       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4065       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4066       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4067       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4068       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4069       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4070       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4071       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4072       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4073       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4074       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4075       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4076       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4077       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4078       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4079       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4080       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4081       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4082       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4083       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4084       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4085       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4086       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4087       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4088       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4089       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4090       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4091       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4092       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4093       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4094       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4095       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4096       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4097       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4098       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4099       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4264       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4265       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4266       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4267       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4268       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4269       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4270       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4271       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4272       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4273       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4274       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4275       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4276       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4277       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4278       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4279       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4280       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4281       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4282       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4283       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4284       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4285       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4286       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4287       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4288       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4289       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4290       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4291       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4292       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4293       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4294       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4295       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4296       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4297       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4298       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4299       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4300       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4301       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4302       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4303       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4304       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4305       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4306       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4307       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4308       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4309       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4310       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4311       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4312       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4313       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4314       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4315       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4316       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4317       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4318       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4319       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4320       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4321       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4322       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4323       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4324       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4325       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4326       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4327       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4328       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4329       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4330       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4331       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4332       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4333       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4334       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4335       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4336       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4337       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4338       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4339       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4340       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4341       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4342       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4343       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4344       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4345       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4346       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4347       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4348       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4349       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4350       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4351       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4352       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4353       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4354       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4355       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4356       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4357       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4358       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4359       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4360       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4361       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4362       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4363       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4364       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4365       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4366       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4367       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4368       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4369       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4370       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4371       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4372       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4373       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4374       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4375       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4376       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4377       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4378       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4379       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4380       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4381       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4382       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4383       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4384       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4385       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4386       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4387       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4388       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4389       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4390       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4391       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4392       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4393       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4394       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4395       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4396       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4397       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4398       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4399       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4400       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4401       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4402       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4403       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4404       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4405       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4406       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4407       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4408       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4409       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4410       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4411       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4412       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4413       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4414       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4415       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4416       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4417       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4418       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4419       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4420       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4421       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4422       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4423       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4424       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4425       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4426       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4427       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4428       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4429       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4430       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4431       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4432       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4433       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4434       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4435       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4436       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4437       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4438       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4439       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4440       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4441       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4442       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4443       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4444       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4445       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4446       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4447       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4448       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4449       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4450       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4451       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4452       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4453       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4454       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4455       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4456       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4457       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4458       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4459       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4460       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4461       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4462       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4463       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4464       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4465       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4466       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4467       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4468       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4469       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4470       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4471       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4472       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4473       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4474       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4475       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4476       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4477       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4478       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4479       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4480       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4481       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4482       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4483       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4484       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4485       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4486       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4487       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4488       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4489       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4490       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4491       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4492       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4493       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4494       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4495       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4496       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4497       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4498       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4499       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4500       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4501       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4502       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4503       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4504       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4505       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4506       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4507       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4508       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4509       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4510       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4511       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4512       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4513       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4514       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4515       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4516       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4517       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4518       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4519       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4520       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4521       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4522       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4523       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4524       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4525       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4526       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4527       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4528       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4529       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4530       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4531       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4532       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4533       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4534       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4535       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4536       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4537       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4538       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4539       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4540       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4541       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4542       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4543       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4544       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4545       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4546       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4547       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4548       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4549       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4550       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4551       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4552       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4553       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4554       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4555       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4556       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4557       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4558       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4559       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4560       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4561       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4562       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4563       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4564       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4565       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4566       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4567       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4568       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4569       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4570       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4571       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4572       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4573       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4574       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4575       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4576       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4577       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4578       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4579       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4580       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4581       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4582       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4583       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4584       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4585       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4586       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4587       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4588       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4589       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4590       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4591       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4592       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4593       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4594       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4595       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4596       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4597       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4598       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4599       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4600       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4601       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4602       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4603       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4604       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4605       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4606       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4607       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4608       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4609       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4610       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4611       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4612       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4613       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4614       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4615       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4616       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4617       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4618       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4619       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4620       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4621       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4622       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4623       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4624       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4625       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4626       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4627       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4628       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4629       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4630       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4631       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4632       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4633       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4634       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4635       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4636       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4637       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4638       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4639       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4640       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4641       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4642       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4643       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4644       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4645       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4646       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4647       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4648       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4649       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4650       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4651       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4652       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4653       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4654       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4655       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4656       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4657       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4658       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4659       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4660       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4661       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4662       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4663       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4664       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4665       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4666       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4667       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4668       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4669       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4670       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4671       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4672       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4673       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4674       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4675       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4676       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4677       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4678       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4679       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4680       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4681       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4682       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4683       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4684       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4685       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4686       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4687       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4688       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4689       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4690       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4691       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4692       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4693       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4694       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4695       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4696       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4697       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4698       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4699       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4700       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4701       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4702       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4703       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4704       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4705       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4706       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4707       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4708       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4709       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4710       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4711       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4712       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4713       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4714       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4715       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4716       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4717       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4718       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4719       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4720       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4721       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4722       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4723       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4724       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4725       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4726       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4727       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4728       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4729       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4730       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4731       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4732       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4733       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4734       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4735       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4736       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4737       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4738       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4739       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4740       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4741       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4742       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4743       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4744       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4745       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4746       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4747       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4748       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4749       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4750       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4751       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4752       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4753       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4754       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4755       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4756       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4757       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4758       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4759       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4760       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4761       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4762       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4763       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4764       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4765       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4766       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4767       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4768       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4769       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4770       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4771       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4772       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4773       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4774       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4775       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4776       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4777       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4778       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4779       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4780       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4781       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4782       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4783       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4784       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4785       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4786       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4787       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4788       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4789       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4790       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4791       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4792       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4793       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4794       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4795       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4796       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4797       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4798       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4799       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4800       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4801       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4802       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4803       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4804       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4805       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4806       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4807       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4808       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4809       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4810       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4811       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4812       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4813       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4814       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4815       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4816       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4817       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4818       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4819       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4820       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4821       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4822       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4823       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4824       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4825       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4826       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4827       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4828       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4829       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4830       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4831       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4832       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4833       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4834       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4835       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4836       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4837       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4838       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4839       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4840       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4841       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4842       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4843       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4844       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4845       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4846       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4847       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4848       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4849       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4850       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4851       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4852       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4853       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4854       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4855       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4856       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4857       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4858       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4859       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4860       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4861       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4862       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4863       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4864       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4865       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4866       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4867       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4868       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4869       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4870       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4871       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4872       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4873       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4874       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4875       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4876       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4877       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4878       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4879       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4880       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4881       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4882       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4883       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4884       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4885       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4886       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4887       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4888       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4889       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4890       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4891       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4892       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4893       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4894       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4895       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4896       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4897       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4898       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4899       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4900       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4901       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4902       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4903       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4904       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4905       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4906       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4907       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4908       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4909       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4910       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4911       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4912       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4913       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4914       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4915       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4916       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4917       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4918       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4919       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4920       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4921       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4922       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4923       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4924       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4925       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4926       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4927       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4928       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4929       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4930       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4931       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4932       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4933       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4934       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4935       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4936       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4937       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4938       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4939       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4940       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4941       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4942       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4943       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4944       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4945       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4946       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4947       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4948       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4949       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4950       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4951       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4952       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4953       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4954       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4955       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4956       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4957       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4958       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4959       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4960       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4961       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4962       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4963       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4964       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4965       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4966       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4967       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4968       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4969       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4970       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4971       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4972       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4973       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4974       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4975       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4976       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4977       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4978       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4979       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4980       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4981       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4982       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4983       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4984       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4985       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4986       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4987       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4988       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4989       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4990       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4991       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4992       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4993       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4994       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4995       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4996       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4997       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4998       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   4999       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5000       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5001       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5002       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5003       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5004       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5005       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5006       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5007       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5008       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5009       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5010       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5011       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5012       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5013       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5014       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5015       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5016       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5017       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5018       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5019       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5020       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5021       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5022       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5023       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5024       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5025       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5026       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5027       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5028       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5029       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5030       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5031       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5032       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5033       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5034       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5035       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5036       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5037       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5038       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5039       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5040       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5041       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5042       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5043       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5044       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5045       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5046       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5047       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5048       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5049       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5050       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5051       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5052       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5053       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5054       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5055       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5056       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5057       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5058       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5059       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5060       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5061       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5062       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5063       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5064       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5065       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5066       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5067       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5068       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5069       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5070       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5071       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5072       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5073       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5074       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5075       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5076       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5077       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5078       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5079       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5080       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5081       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5082       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5083       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5084       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5085       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5086       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5087       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5088       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5089       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5090       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5091       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5092       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5093       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5094       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5095       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5096       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5097       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5098       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5099       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5100       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5101       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5102       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5103       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5104       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5105       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5106       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5107       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5108       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5109       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5110       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5111       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5112       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5113       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5114       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5115       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5116       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5117       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5118       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5119       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5120       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5121       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5122       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5123       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5124       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5125       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5126       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5127       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5128       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5129       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5130       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5131       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5132       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5133       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5134       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5135       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5136       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5137       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5138       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5139       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5140       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5141       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5142       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5143       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5144       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5145       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5146       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5147       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5148       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5149       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5150       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5151       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5152       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5153       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5154       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5155       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5156       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5157       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5158       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5159       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5160       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5161       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5162       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5163       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5164       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5165       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5166       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5167       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5168       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5169       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5170       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5171       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5172       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5173       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5174       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5175       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5176       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5177       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5178       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5179       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5180       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5181       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5182       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5183       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5184       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5185       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5186       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5187       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5188       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5189       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5190       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5191       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5192       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5193       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5194       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5195       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5196       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5197       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5198       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5199       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5200       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5201       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5202       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5203       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5204       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5205       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5206       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5207       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5208       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5209       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5210       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5211       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5212       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5213       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5214       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5215       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5216       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5217       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5218       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5219       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5220       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5221       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5222       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5223       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5224       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5225       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5226       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5227       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5228       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5229       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5230       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5231       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5232       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5233       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5234       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5235       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5236       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5237       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5238       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5239       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5240       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5241       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5242       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5243       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5244       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5245       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5246       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5247       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5248       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5249       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5250       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5251       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5252       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5253       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5254       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5255       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5256       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5257       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5258       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5259       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5260       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5261       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5262       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##   5263       NA    NA     NA   NA       NA   NA   NA       NA   NA    NA
    ##           [,11] [,12] [,13]  [,14] [,15]   [,16]  [,17]  [,18]        [,19]
    ##      1       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      2       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      3       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      4       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      5       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      6       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      7       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      8       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##      9       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     10       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     11       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     12       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     13       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     14       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     15       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     16       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     17       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     18       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     19       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     20       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     21       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     22       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     23       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     24       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     25       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     26       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     27       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     28       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     29       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     30       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     31       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     32       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     33       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     34       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     35       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     36       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     37       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     38       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     39       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     40       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     41       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     42       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     43       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     44       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     45       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     46       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     47       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     48       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     49       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     50       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     51       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     52       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     53       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     54       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     55       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     56       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     57       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     58       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     59       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     60       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     61       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     62       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     63       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     64       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     65       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     66       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     67       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     68       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     69       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     70       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     71       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     72       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     73       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     74       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     75       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     76       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     77       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     78       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     79       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     80       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     81       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     82       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     83       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     84       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     85       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     86       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     87       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     88       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     89       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     90       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     91       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     92       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     93       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     94       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     95       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     96       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     97       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     98       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##     99       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    264       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    265       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    266       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    267       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    268       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    269       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    270       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    271       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    272       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    273       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    274       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    275       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    276       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    277       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    278       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    279       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    280       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    281       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    282       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    283       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    284       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    285       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    286       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    287       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    288       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    289       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    290       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    291       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    292       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    293       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    294       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    295       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    296       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    297       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    298       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    299       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    300       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    301       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    302       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    303       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    304       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    305       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    306       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    307       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    308       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    309       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    310       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    311       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    312       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    313       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    314       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    315       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    316       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    317       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    318       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    319       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    320       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    321       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    322       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    323       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    324       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    325       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    326       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    327       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    328       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    329       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    330       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    331       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    332       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    333       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    334       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    335       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    336       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    337       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    338       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    339       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    340       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    341       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    342       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    343       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    344       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    345       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    346       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    347       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    348       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    349       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    350       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    351       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    352       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    353       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    354       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    355       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    356       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    357       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    358       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    359       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    360       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    361       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    362       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    363       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    364       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    365       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    366       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    367       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    368       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    369       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    370       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    371       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    372       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    373       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    374       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    375       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    376       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    377       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    378       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    379       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    380       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    381       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    382       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    383       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    384       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    385       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    386       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    387       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    388       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    389       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    390       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    391       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    392       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    393       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    394       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    395       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    396       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    397       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    398       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    399       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    400       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    401       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    402       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    403       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    404       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    405       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    406       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    407       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    408       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    409       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    410       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    411       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    412       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    413       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    414       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    415       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    416       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    417       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    418       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    419       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    420       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    421       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    422       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    423       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    424       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    425       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    426       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    427       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    428       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    429       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    430       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    431       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    432       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    433       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    434       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    435       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    436       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    437       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    438       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    439       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    440       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    441       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    442       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    443       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    444       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    445       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    446       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    447       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    448       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    449       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    450       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    451       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    452       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    453       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    454       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    455       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    456       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    457       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    458       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    459       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    460       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    461       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    462       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    463       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    464       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    465       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    466       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    467       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    468       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    469       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    470       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    471       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    472       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    473       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    474       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    475       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    476       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    477       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    478       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    479       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    480       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    481       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    482       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    483       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    484       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    485       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    486       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    487       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    488       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    489       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    490       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    491       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    492       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    493       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    494       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    495       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    496       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    497       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    498       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    499       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    500       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    501       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    502       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    503       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    504       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    505       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    506       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    507       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    508       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    509       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    510       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    511       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    512       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    513       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    514       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    515       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    516       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    517       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    518       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    519       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    520       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    521       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    522       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    523       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    524       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    525       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    526       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    527       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    528       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    529       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    530       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    531       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    532       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    533       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    534       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    535       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    536       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    537       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    538       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    539       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    540       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    541       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    542       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    543       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    544       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    545       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    546       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    547       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    548       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    549       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    550       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    551       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    552       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    553       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    554       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    555       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    556       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    557       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    558       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    559       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    560       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    561       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    562       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    563       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    564       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    565       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    566       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    567       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    568       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    569       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    570       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    571       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    572       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    573       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    574       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    575       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    576       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    577       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    578       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    579       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    580       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    581       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    582       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    583       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    584       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    585       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    586       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    587       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    588       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    589       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    590       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    591       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    592       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    593       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    594       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    595       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    596       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    597       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    598       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    599       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    600       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    601       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    602       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    603       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    604       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    605       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    606       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    607       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    608       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    609       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    610       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    611       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    612       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    613       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    614       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    615       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    616       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    617       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    618       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    619       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    620       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    621       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    622       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    623       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    624       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    625       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    626       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    627       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    628       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    629       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    630       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    631       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    632       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    633       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    634       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    635       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    636       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    637       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    638       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    639       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    640       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    641       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    642       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    643       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    644       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    645       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    646       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    647       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    648       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    649       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    650       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    651       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    652       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    653       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    654       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    655       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    656       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    657       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    658       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    659       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    660       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    661       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    662       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    663       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    664       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    665       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    666       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    667       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    668       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    669       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    670       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    671       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    672       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    673       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    674       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    675       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    676       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    677       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    678       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    679       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    680       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    681       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    682       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    683       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    684       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    685       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    686       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    687       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    688       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    689       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    690       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    691       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    692       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    693       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    694       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    695       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    696       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    697       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    698       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    699       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    700       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    701       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    702       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    703       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    704       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    705       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    706       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    707       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    708       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    709       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    710       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    711       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    712       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    713       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    714       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    715       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    716       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    717       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    718       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    719       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    720       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    721       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    722       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    723       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    724       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    725       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    726       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    727       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    728       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    729       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    730       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    731       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    732       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    733       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    734       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    735       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    736       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    737       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    738       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    739       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    740       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    741       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    742       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    743       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    744       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    745       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    746       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    747       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    748       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    749       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    750       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    751       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    752       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    753       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    754       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    755       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    756       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    757       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    758       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    759       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    760       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    761       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    762       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    763       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    764       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    765       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    766       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    767       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    768       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    769       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    770       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    771       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    772       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    773       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    774       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    775       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    776       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    777       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    778       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    779       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    780       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    781       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    782       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    783       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    784       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    785       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    786       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    787       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    788       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    789       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    790       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    791       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    792       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    793       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    794       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    795       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    796       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    797       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    798       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    799       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    800       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    801       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    802       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    803       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    804       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    805       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    806       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    807       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    808       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    809       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    810       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    811       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    812       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    813       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    814       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    815       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    816       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    817       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    818       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    819       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    820       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    821       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    822       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    823       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    824       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    825       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    826       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    827       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    828       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    829       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    830       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    831       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    832       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    833       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    834       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    835       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    836       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    837       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    838       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    839       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    840       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    841       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    842       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    843       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    844       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    845       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    846       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    847       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    848       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    849       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    850       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    851       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    852       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    853       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    854       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    855       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    856       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    857       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    858       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    859       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    860       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    861       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    862       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    863       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    864       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    865       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    866       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    867       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    868       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    869       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    870       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    871       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    872       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    873       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    874       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    875       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    876       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    877       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    878       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    879       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    880       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    881       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    882       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    883       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    884       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    885       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    886       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    887       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    888       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    889       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    890       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    891       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    892       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    893       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    894       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    895       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    896       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    897       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    898       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    899       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    900       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    901       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    902       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    903       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    904       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    905       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    906       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    907       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    908       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    909       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    910       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    911       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    912       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    913       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    914       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    915       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    916       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    917       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    918       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    919       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    920       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    921       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    922       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    923       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    924       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    925       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    926       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    927       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    928       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    929       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    930       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    931       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    932       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    933       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    934       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    935       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    936       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    937       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    938       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    939       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    940       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    941       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    942       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    943       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    944       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    945       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    946       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    947       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    948       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    949       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    950       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    951       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    952       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    953       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    954       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    955       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    956       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    957       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    958       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    959       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    960       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    961       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    962       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    963       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    964       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    965       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    966       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    967       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    968       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    969       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    970       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    971       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    972       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    973       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    974       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    975       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    976       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    977       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    978       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    979       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    980       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    981       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    982       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    983       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    984       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    985       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    986       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    987       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    988       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    989       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    990       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    991       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    992       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    993       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    994       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    995       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    996       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    997       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    998       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##    999       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1000       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1001       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1002       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1003       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1004       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1005       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1006       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1007       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1008       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1009       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1010       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1011       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1012       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1013       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1014       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1015       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1016       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1017       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1018       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1019       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1020       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1021       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1022       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1023       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1024       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1025       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1026       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1027       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1028       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1029       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1030       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1031       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1032       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1033       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1034       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1035       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1036       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1037       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1038       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1039       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1040       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1041       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1042       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1043       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1044       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1045       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1046       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1047       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1048       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1049       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1050       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1051       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1052       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1053       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1054       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1055       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1056       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1057       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1058       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1059       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1060       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1061       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1062       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1063       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1064       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1065       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1066       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1067       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1068       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1069       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1070       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1071       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1072       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1073       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1074       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1075       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1076       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1077       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1078       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1079       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1080       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1081       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1082       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1083       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1084       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1085       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1086       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1087       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1088       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1089       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1090       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1091       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1092       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1093       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1094       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1095       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1096       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1097       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1098       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1099       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1264       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1265       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1266       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1267       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1268       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1269       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1270       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1271       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1272       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1273       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1274       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1275       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1276       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1277       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1278       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1279       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1280       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1281       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1282       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1283       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1284       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1285       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1286       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1287       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1288       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1289       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1290       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1291       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1292       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1293       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1294       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1295       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1296       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1297       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1298       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1299       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1300       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1301       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1302       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1303       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1304       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1305       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1306       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1307       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1308       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1309       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1310       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1311       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1312       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1313       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1314       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1315       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1316       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1317       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1318       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1319       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1320       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1321       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1322       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1323       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1324       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1325       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1326       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1327       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1328       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1329       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1330       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1331       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1332       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1333       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1334       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1335       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1336       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1337       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1338       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1339       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1340       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1341       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1342       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1343       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1344       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1345       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1346       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1347       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1348       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1349       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1350       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1351       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1352       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1353       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1354       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1355       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1356       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1357       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1358       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1359       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1360       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1361       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1362       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1363       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1364       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1365       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1366       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1367       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1368       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1369       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1370       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1371       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1372       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1373       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1374       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1375       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1376       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1377       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1378       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1379       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1380       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1381       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1382       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1383       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1384       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1385       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1386       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1387       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1388       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1389       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1390       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1391       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1392       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1393       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1394       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1395       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1396       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1397       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1398       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1399       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1400       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1401       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1402       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1403       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1404       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1405       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1406       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1407       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1408       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1409       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1410       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1411       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1412       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1413       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1414       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1415       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1416       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1417       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1418       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1419       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1420       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1421       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1422       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1423       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1424       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1425       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1426       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1427       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1428       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1429       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1430       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1431       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1432       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1433       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1434       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1435       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1436       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1437       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1438       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1439       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1440       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1441       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1442       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1443       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1444       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1445       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1446       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1447       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1448       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1449       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1450       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1451       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1452       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1453       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1454       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1455       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1456       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1457       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1458       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1459       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1460       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1461       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1462       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1463       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1464       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1465       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1466       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1467       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1468       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1469       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1470       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1471       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1472       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1473       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1474       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1475       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1476       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1477       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1478       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1479       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1480       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1481       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1482       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1483       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1484       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1485       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1486       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1487       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1488       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1489       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1490       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1491       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1492       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1493       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1494       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1495       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1496       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1497       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1498       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1499       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1500       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1501       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1502       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1503       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1504       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1505       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1506       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1507       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1508       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1509       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1510       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1511       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1512       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1513       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1514       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1515       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1516       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1517       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1518       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1519       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1520       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1521       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1522       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1523       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1524       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1525       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1526       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1527       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1528       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1529       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1530       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1531       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1532       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1533       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1534       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1535       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1536       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1537       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1538       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1539       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1540       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1541       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1542       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1543       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1544       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1545       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1546       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1547       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1548       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1549       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1550       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1551       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1552       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1553       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1554       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1555       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1556       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1557       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1558       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1559       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1560       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1561       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1562       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1563       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1564       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1565       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1566       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1567       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1568       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1569       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1570       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1571       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1572       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1573       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1574       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1575       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1576       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1577       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1578       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1579       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1580       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1581       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1582       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1583       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1584       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1585       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1586       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1587       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1588       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1589       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1590       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1591       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1592       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1593       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1594       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1595       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1596       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1597       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1598       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1599       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1600       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1601       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1602       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1603       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1604       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1605       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1606       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1607       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1608       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1609       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1610       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1611       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1612       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1613       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1614       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1615       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1616       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1617       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1618       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1619       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1620       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1621       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1622       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1623       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1624       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1625       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1626       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1627       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1628       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1629       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1630       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1631       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1632       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1633       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1634       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1635       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1636       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1637       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1638       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1639       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1640       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1641       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1642       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1643       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1644       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1645       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1646       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1647       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1648       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1649       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1650       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1651       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1652       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1653       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1654       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1655       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1656       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1657       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1658       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1659       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1660       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1661       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1662       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1663       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1664       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1665       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1666       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1667       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1668       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1669       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1670       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1671       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1672       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1673       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1674       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1675       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1676       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1677       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1678       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1679       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1680       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1681       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1682       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1683       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1684       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1685       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1686       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1687       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1688       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1689       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1690       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1691       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1692       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1693       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1694       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1695       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1696       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1697       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1698       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1699       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1700       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1701       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1702       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1703       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1704       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1705       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1706       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1707       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1708       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1709       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1710       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1711       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1712       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1713       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1714       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1715       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1716       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1717       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1718       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1719       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1720       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1721       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1722       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1723       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1724       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1725       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1726       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1727       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1728       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1729       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1730       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1731       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1732       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1733       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1734       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1735       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1736       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1737       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1738       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1739       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1740       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1741       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1742       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1743       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1744       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1745       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1746       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1747       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1748       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1749       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1750       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1751       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1752       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1753       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1754       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1755       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1756       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1757       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1758       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1759       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1760       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1761       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1762       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1763       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1764       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1765       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1766       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1767       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1768       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1769       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1770       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1771       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1772       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1773       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1774       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1775       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1776       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1777       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1778       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1779       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1780       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1781       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1782       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1783       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1784       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1785       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1786       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1787       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1788       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1789       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1790       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1791       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1792       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1793       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1794       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1795       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1796       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1797       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1798       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1799       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1800       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1801       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1802       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1803       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1804       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1805       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1806       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1807       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1808       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1809       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1810       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1811       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1812       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1813       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1814       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1815       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1816       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1817       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1818       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1819       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1820       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1821       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1822       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1823       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1824       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1825       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1826       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1827       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1828       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1829       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1830       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1831       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1832       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1833       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1834       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1835       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1836       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1837       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1838       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1839       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1840       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1841       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1842       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1843       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1844       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1845       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1846       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1847       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1848       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1849       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1850       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1851       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1852       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1853       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1854       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1855       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1856       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1857       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1858       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1859       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1860       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1861       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1862       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1863       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1864       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1865       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1866       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1867       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1868       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1869       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1870       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1871       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1872       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1873       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1874       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1875       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1876       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1877       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1878       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1879       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1880       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1881       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1882       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1883       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1884       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1885       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1886       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1887       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1888       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1889       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1890       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1891       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1892       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1893       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1894       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1895       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1896       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1897       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1898       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1899       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1900       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1901       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1902       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1903       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1904       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1905       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1906       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1907       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1908       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1909       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1910       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1911       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1912       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1913       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1914       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1915       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1916       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1917       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1918       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1919       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1920       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1921       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1922       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1923       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1924       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1925       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1926       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1927       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1928       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1929       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1930       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1931       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1932       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1933       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1934       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1935       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1936       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1937       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1938       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1939       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1940       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1941       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1942       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1943       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1944       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1945       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1946       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1947       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1948       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1949       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1950       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1951       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1952       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1953       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1954       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1955       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1956       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1957       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1958       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1959       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1960       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1961       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1962       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1963       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1964       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1965       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1966       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1967       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1968       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1969       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1970       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1971       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1972       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1973       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1974       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1975       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1976       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1977       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1978       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1979       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1980       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1981       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1982       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1983       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1984       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1985       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1986       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1987       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1988       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1989       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1990       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1991       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1992       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1993       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1994       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1995       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1996       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1997       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1998       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   1999       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2000       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2001       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2002       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2003       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2004       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2005       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2006       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2007       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2008       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2009       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2010       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2011       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2012       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2013       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2014       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2015       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2016       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2017       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2018       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2019       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2020       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2021       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2022       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2023       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2024       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2025       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2026       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2027       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2028       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2029       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2030       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2031       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2032       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2033       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2034       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2035       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2036       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2037       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2038       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2039       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2040       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2041       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2042       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2043       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2044       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2045       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2046       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2047       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2048       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2049       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2050       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2051       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2052       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2053       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2054       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2055       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2056       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2057       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2058       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2059       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2060       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2061       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2062       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2063       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2064       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2065       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2066       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2067       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2068       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2069       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2070       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2071       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2072       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2073       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2074       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2075       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2076       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2077       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2078       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2079       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2080       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2081       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2082       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2083       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2084       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2085       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2086       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2087       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2088       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2089       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2090       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2091       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2092       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2093       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2094       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2095       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2096       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2097       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2098       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2099       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2264       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2265       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2266       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2267       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2268       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2269       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2270       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2271       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2272       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2273       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2274       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2275       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2276       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2277       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2278       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2279       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2280       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2281       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2282       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2283       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2284       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2285       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2286       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2287       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2288       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2289       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2290       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2291       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2292       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2293       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2294       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2295       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2296       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2297       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2298       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2299       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2300       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2301       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2302       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2303       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2304       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2305       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2306       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2307       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2308       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2309       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2310       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2311       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2312       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2313       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2314       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2315       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2316       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2317       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2318       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2319       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2320       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2321       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2322       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2323       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2324       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2325       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2326       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2327       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2328       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2329       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2330       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2331       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2332       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2333       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2334       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2335       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2336       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2337       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2338       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2339       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2340       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2341       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2342       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2343       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2344       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2345       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2346       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2347       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2348       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2349       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2350       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2351       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2352       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2353       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2354       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2355       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2356       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2357       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2358       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2359       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2360       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2361       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2362       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2363       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2364       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2365       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2366       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2367       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2368       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2369       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2370       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2371       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2372       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2373       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2374       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2375       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2376       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2377       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2378       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2379       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2380       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2381       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2382       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2383       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2384       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2385       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2386       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2387       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2388       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2389       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2390       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2391       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2392       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2393       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2394       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2395       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2396       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2397       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2398       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2399       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2400       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2401       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2402       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2403       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2404       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2405       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2406       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2407       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2408       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2409       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2410       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2411       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2412       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2413       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2414       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2415       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2416       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2417       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2418       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2419       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2420       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2421       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2422       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2423       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2424       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2425       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2426       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2427       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2428       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2429       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2430       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2431       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2432       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2433       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2434       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2435       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2436       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2437       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2438       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2439       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2440       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2441       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2442       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2443       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2444       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2445       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2446       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2447       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2448       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2449       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2450       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2451       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2452       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2453       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2454       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2455       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2456       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2457       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2458       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2459       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2460       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2461       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2462       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2463       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2464       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2465       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2466       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2467       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2468       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2469       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2470       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2471       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2472       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2473       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2474       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2475       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2476       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2477       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2478       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2479       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2480       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2481       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2482       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2483       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2484       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2485       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2486       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2487       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2488       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2489       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2490       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2491       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2492       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2493       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2494       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2495       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2496       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2497       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2498       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2499       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2500       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2501       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2502       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2503       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2504       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2505       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2506       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2507       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2508       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2509       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2510       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2511       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2512       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2513       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2514       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2515       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2516       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2517       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2518       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2519       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2520       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2521       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2522       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2523       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2524       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2525       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2526       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2527       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2528       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2529       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2530       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2531       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2532       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2533       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2534       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2535       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2536       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2537       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2538       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2539       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2540       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2541       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2542       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2543       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2544       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2545       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2546       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2547       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2548       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2549       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2550       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2551       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2552       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2553       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2554       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2555       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2556       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2557       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2558       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2559       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2560       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2561       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2562       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2563       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2564       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2565       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2566       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2567       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2568       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2569       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2570       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2571       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2572       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2573       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2574       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2575       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2576       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2577       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2578       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2579       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2580       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2581       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2582       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2583       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2584       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2585       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2586       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2587       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2588       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2589       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2590       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2591       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2592       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2593       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2594       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2595       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2596       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2597       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2598       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2599       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2600       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2601       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2602       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2603       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2604       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2605       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2606       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2607       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2608       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2609       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2610       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2611       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2612       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2613       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2614       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2615       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2616       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2617       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2618       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2619       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2620       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2621       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2622       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2623       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2624       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2625       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2626       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2627       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2628       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2629       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2630       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2631       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2632       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2633       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2634       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2635       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2636       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2637       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2638       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2639       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2640       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2641       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2642       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2643       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2644       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2645       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2646       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2647       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2648       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2649       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2650       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2651       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2652       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2653       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2654       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2655       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2656       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2657       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2658       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2659       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2660       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2661       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2662       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2663       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2664       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2665       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2666       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2667       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2668       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2669       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2670       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2671       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2672       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2673       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2674       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2675       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2676       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2677       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2678       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2679       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2680       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2681       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2682       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2683       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2684       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2685       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2686       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2687       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2688       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2689       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2690       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2691       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2692       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2693       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2694       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2695       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2696       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2697       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2698       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2699       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2700       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2701       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2702       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2703       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2704       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2705       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2706       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2707       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2708       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2709       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2710       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2711       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2712       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2713       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2714       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2715       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2716       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2717       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2718       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2719       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2720       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2721       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2722       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2723       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2724       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2725       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2726       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2727       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2728       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2729       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2730       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2731       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2732       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2733       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2734       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2735       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2736       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2737       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2738       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2739       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2740       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2741       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2742       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2743       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2744       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2745       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2746       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2747       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2748       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2749       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2750       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2751       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2752       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2753       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2754       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2755       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2756       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2757       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2758       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2759       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2760       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2761       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2762       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2763       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2764       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2765       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2766       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2767       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2768       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2769       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2770       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2771       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2772       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2773       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2774       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2775       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2776       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2777       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2778       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2779       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2780       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2781       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2782       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2783       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2784       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2785       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2786       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2787       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2788       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2789       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2790       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2791       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2792       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2793       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2794       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2795       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2796       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2797       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2798       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2799       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2800       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2801       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2802       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2803       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2804       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2805       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2806       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2807       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2808       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2809       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2810       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2811       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2812       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2813       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2814       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2815       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2816       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2817       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2818       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2819       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2820       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2821       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2822       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2823       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2824       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2825       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2826       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2827       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2828       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2829       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2830       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2831       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2832       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2833       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2834       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2835       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2836       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2837       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2838       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2839       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2840       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2841       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2842       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2843       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2844       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2845       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2846       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2847       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2848       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2849       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2850       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2851       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2852       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2853       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2854       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2855       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2856       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2857       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2858       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2859       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2860       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2861       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2862       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2863       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2864       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2865       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2866       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2867       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2868       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2869       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2870       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2871       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2872       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2873       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2874       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2875       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2876       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2877       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2878       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2879       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2880       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2881       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2882       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2883       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2884       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2885       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2886       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2887       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2888       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2889       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2890       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2891       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2892       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2893       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2894       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2895       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2896       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2897       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2898       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2899       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2900       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2901       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2902       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2903       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2904       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2905       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2906       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2907       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2908       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2909       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2910       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2911       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2912       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2913       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2914       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2915       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2916       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2917       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2918       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2919       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2920       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2921       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2922       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2923       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2924       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2925       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2926       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2927       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2928       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2929       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2930       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2931       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2932       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2933       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2934       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2935       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2936       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2937       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2938       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2939       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2940       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2941       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2942       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2943       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2944       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2945       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2946       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2947       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2948       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2949       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2950       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2951       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2952       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2953       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2954       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2955       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2956       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2957       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2958       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2959       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2960       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2961       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2962       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2963       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2964       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2965       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2966       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2967       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2968       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2969       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2970       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2971       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2972       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2973       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2974       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2975       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2976       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2977       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2978       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2979       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2980       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2981       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2982       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2983       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2984       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2985       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2986       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2987       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2988       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2989       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2990       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2991       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2992       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2993       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2994       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2995       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2996       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2997       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2998       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   2999       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3000       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3001       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3002       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3003       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3004       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3005       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3006       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3007       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3008       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3009       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3010       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3011       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3012       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3013       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3014       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3015       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3016       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3017       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3018       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3019       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3020       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3021       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3022       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3023       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3024       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3025       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3026       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3027       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3028       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3029       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3030       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3031       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3032       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3033       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3034       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3035       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3036       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3037       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3038       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3039       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3040       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3041       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3042       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3043       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3044       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3045       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3046       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3047       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3048       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3049       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3050       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3051       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3052       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3053       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3054       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3055       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3056       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3057       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3058       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3059       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3060       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3061       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3062       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3063       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3064       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3065       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3066       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3067       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3068       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3069       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3070       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3071       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3072       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3073       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3074       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3075       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3076       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3077       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3078       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3079       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3080       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3081       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3082       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3083       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3084       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3085       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3086       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3087       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3088       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3089       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3090       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3091       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3092       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3093       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3094       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3095       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3096       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3097       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3098       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3099       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3264       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3265       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3266       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3267       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3268       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3269       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3270       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3271       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3272       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3273       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3274       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3275       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3276       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3277       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3278       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3279       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3280       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3281       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3282       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3283       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3284       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3285       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3286       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3287       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3288       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3289       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3290       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3291       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3292       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3293       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3294       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3295       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3296       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3297       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3298       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3299       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3300       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3301       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3302       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3303       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3304       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3305       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3306       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3307       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3308       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3309       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3310       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3311       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3312       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3313       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3314       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3315       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3316       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3317       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3318       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3319       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3320       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3321       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3322       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3323       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3324       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3325       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3326       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3327       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3328       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3329       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3330       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3331       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3332       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3333       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3334       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3335       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3336       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3337       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3338       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3339       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3340       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3341       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3342       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3343       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3344       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3345       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3346       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3347       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3348       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3349       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3350       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3351       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3352       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3353       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3354       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3355       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3356       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3357       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3358       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3359       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3360       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3361       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3362       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3363       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3364       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3365       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3366       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3367       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3368       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3369       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3370       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3371       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3372       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3373       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3374       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3375       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3376       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3377       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3378       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3379       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3380       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3381       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3382       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3383       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3384       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3385       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3386       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3387       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3388       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3389       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3390       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3391       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3392       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3393       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3394       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3395       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3396       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3397       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3398       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3399       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3400       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3401       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3402       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3403       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3404       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3405       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3406       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3407       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3408       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3409       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3410       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3411       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3412       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3413       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3414       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3415       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3416       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3417       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3418       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3419       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3420       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3421       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3422       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3423       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3424       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3425       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3426       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3427       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3428       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3429       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3430       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3431       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3432       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3433       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3434       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3435       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3436       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3437       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3438       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3439       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3440       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3441       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3442       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3443       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3444       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3445       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3446       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3447       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3448       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3449       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3450       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3451       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3452       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3453       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3454       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3455       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3456       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3457       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3458       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3459       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3460       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3461       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3462       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3463       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3464       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3465       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3466       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3467       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3468       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3469       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3470       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3471       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3472       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3473       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3474       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3475       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3476       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3477       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3478       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3479       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3480       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3481       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3482       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3483       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3484       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3485       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3486       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3487       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3488       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3489       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3490       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3491       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3492       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3493       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3494       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3495       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3496       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3497       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3498       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3499       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3500       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3501       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3502       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3503       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3504       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3505       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3506       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3507       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3508       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3509       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3510       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3511       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3512       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3513       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3514       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3515       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3516       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3517       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3518       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3519       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3520       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3521       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3522       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3523       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3524       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3525       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3526       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3527       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3528       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3529       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3530       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3531       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3532       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3533       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3534       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3535       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3536       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3537       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3538       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3539       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3540       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3541       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3542       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3543       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3544       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3545       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3546       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3547       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3548       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3549       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3550       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3551       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3552       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3553       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3554       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3555       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3556       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3557       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3558       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3559       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3560       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3561       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3562       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3563       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3564       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3565       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3566       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3567       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3568       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3569       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3570       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3571       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3572       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3573       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3574       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3575       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3576       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3577       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3578       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3579       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3580       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3581       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3582       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3583       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3584       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3585       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3586       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3587       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3588       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3589       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3590       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3591       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3592       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3593       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3594       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3595       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3596       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3597       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3598       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3599       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3600       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3601       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3602       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3603       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3604       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3605       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3606       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3607       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3608       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3609       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3610       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3611       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3612       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3613       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3614       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3615       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3616       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3617       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3618       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3619       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3620       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3621       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3622       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3623       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3624       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3625       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3626       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3627       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3628       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3629       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3630       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3631       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3632       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3633       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3634       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3635       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3636       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3637       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3638       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3639       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3640       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3641       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3642       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3643       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3644       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3645       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3646       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3647       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3648       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3649       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3650       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3651       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3652       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3653       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3654       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3655       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3656       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3657       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3658       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3659       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3660       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3661       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3662       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3663       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3664       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3665       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3666       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3667       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3668       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3669       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3670       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3671       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3672       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3673       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3674       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3675       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3676       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3677       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3678       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3679       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3680       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3681       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3682       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3683       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3684       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3685       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3686       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3687       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3688       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3689       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3690       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3691       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3692       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3693       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3694       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3695       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3696       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3697       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3698       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3699       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3700       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3701       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3702       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3703       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3704       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3705       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3706       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3707       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3708       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3709       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3710       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3711       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3712       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3713       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3714       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3715       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3716       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3717       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3718       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3719       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3720       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3721       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3722       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3723       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3724       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3725       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3726       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3727       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3728       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3729       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3730       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3731       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3732       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3733       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3734       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3735       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3736       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3737       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3738       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3739       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3740       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3741       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3742       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3743       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3744       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3745       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3746       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3747       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3748       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3749       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3750       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3751       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3752       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3753       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3754       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3755       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3756       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3757       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3758       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3759       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3760       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3761       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3762       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3763       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3764       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3765       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3766       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3767       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3768       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3769       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3770       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3771       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3772       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3773       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3774       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3775       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3776       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3777       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3778       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3779       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3780       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3781       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3782       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3783       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3784       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3785       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3786       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3787       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3788       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3789       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3790       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3791       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3792       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3793       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3794       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3795       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3796       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3797       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3798       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3799       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3800       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3801       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3802       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3803       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3804       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3805       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3806       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3807       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3808       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3809       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3810       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3811       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3812       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3813       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3814       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3815       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3816       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3817       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3818       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3819       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3820       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3821       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3822       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3823       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3824       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3825       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3826       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3827       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3828       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3829       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3830       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3831       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3832       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3833       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3834       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3835       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3836       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3837       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3838       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3839       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3840       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3841       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3842       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3843       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3844       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3845       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3846       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3847       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3848       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3849       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3850       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3851       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3852       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3853       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3854       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3855       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3856       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3857       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3858       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3859       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3860       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3861       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3862       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3863       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3864       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3865       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3866       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3867       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3868       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3869       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3870       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3871       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3872       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3873       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3874       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3875       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3876       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3877       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3878       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3879       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3880       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3881       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3882       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3883       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3884       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3885       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3886       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3887       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3888       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3889       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3890       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3891       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3892       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3893       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3894       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3895       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3896       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3897       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3898       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3899       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3900       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3901       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3902       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3903       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3904       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3905       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3906       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3907       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3908       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3909       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3910       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3911       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3912       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3913       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3914       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3915       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3916       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3917       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3918       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3919       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3920       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3921       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3922       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3923       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3924       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3925       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3926       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3927       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3928       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3929       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3930       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3931       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3932       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3933       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3934       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3935       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3936       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3937       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3938       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3939       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3940       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3941       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3942       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3943       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3944       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3945       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3946       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3947       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3948       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3949       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3950       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3951       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3952       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3953       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3954       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3955       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3956       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3957       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3958       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3959       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3960       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3961       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3962       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3963       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3964       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3965       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3966       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3967       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3968       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3969       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3970       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3971       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3972       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3973       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3974       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3975       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3976       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3977       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3978       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3979       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3980       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3981       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3982       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3983       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3984       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3985       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3986       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3987       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3988       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3989       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3990       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3991       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3992       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3993       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3994       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3995       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3996       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3997       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3998       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   3999       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4000       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4001       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4002       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4003       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4004       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4005       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4006       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4007       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4008       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4009       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4010       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4011       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4012       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4013       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4014       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4015       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4016       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4017       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4018       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4019       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4020       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4021       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4022       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4023       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4024       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4025       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4026       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4027       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4028       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4029       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4030       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4031       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4032       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4033       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4034       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4035       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4036       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4037       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4038       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4039       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4040       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4041       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4042       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4043       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4044       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4045       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4046       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4047       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4048       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4049       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4050       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4051       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4052       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4053       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4054       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4055       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4056       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4057       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4058       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4059       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4060       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4061       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4062       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4063       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4064       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4065       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4066       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4067       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4068       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4069       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4070       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4071       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4072       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4073       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4074       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4075       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4076       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4077       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4078       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4079       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4080       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4081       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4082       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4083       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4084       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4085       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4086       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4087       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4088       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4089       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4090       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4091       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4092       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4093       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4094       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4095       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4096       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4097       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4098       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4099       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4264       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4265       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4266       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4267       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4268       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4269       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4270       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4271       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4272       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4273       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4274       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4275       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4276       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4277       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4278       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4279       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4280       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4281       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4282       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4283       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4284       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4285       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4286       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4287       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4288       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4289       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4290       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4291       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4292       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4293       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4294       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4295       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4296       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4297       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4298       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4299       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4300       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4301       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4302       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4303       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4304       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4305       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4306       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4307       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4308       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4309       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4310       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4311       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4312       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4313       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4314       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4315       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4316       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4317       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4318       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4319       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4320       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4321       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4322       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4323       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4324       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4325       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4326       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4327       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4328       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4329       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4330       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4331       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4332       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4333       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4334       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4335       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4336       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4337       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4338       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4339       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4340       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4341       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4342       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4343       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4344       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4345       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4346       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4347       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4348       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4349       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4350       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4351       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4352       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4353       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4354       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4355       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4356       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4357       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4358       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4359       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4360       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4361       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4362       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4363       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4364       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4365       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4366       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4367       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4368       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4369       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4370       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4371       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4372       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4373       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4374       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4375       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4376       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4377       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4378       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4379       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4380       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4381       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4382       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4383       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4384       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4385       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4386       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4387       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4388       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4389       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4390       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4391       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4392       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4393       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4394       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4395       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4396       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4397       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4398       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4399       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4400       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4401       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4402       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4403       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4404       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4405       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4406       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4407       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4408       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4409       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4410       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4411       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4412       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4413       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4414       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4415       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4416       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4417       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4418       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4419       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4420       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4421       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4422       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4423       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4424       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4425       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4426       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4427       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4428       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4429       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4430       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4431       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4432       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4433       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4434       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4435       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4436       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4437       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4438       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4439       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4440       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4441       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4442       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4443       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4444       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4445       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4446       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4447       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4448       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4449       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4450       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4451       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4452       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4453       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4454       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4455       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4456       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4457       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4458       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4459       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4460       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4461       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4462       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4463       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4464       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4465       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4466       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4467       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4468       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4469       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4470       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4471       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4472       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4473       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4474       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4475       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4476       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4477       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4478       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4479       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4480       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4481       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4482       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4483       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4484       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4485       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4486       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4487       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4488       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4489       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4490       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4491       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4492       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4493       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4494       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4495       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4496       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4497       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4498       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4499       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4500       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4501       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4502       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4503       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4504       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4505       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4506       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4507       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4508       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4509       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4510       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4511       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4512       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4513       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4514       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4515       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4516       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4517       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4518       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4519       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4520       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4521       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4522       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4523       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4524       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4525       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4526       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4527       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4528       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4529       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4530       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4531       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4532       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4533       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4534       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4535       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4536       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4537       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4538       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4539       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4540       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4541       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4542       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4543       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4544       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4545       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4546       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4547       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4548       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4549       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4550       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4551       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4552       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4553       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4554       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4555       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4556       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4557       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4558       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4559       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4560       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4561       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4562       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4563       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4564       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4565       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4566       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4567       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4568       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4569       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4570       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4571       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4572       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4573       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4574       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4575       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4576       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4577       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4578       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4579       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4580       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4581       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4582       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4583       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4584       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4585       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4586       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4587       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4588       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4589       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4590       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4591       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4592       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4593       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4594       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4595       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4596       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4597       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4598       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4599       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4600       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4601       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4602       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4603       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4604       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4605       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4606       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4607       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4608       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4609       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4610       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4611       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4612       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4613       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4614       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4615       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4616       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4617       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4618       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4619       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4620       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4621       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4622       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4623       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4624       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4625       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4626       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4627       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4628       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4629       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4630       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4631       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4632       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4633       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4634       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4635       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4636       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4637       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4638       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4639       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4640       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4641       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4642       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4643       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4644       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4645       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4646       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4647       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4648       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4649       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4650       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4651       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4652       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4653       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4654       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4655       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4656       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4657       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4658       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4659       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4660       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4661       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4662       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4663       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4664       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4665       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4666       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4667       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4668       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4669       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4670       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4671       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4672       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4673       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4674       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4675       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4676       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4677       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4678       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4679       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4680       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4681       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4682       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4683       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4684       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4685       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4686       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4687       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4688       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4689       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4690       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4691       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4692       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4693       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4694       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4695       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4696       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4697       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4698       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4699       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4700       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4701       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4702       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4703       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4704       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4705       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4706       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4707       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4708       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4709       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4710       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4711       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4712       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4713       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4714       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4715       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4716       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4717       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4718       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4719       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4720       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4721       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4722       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4723       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4724       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4725       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4726       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4727       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4728       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4729       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4730       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4731       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4732       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4733       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4734       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4735       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4736       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4737       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4738       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4739       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4740       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4741       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4742       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4743       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4744       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4745       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4746       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4747       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4748       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4749       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4750       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4751       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4752       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4753       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4754       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4755       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4756       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4757       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4758       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4759       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4760       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4761       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4762       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4763       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4764       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4765       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4766       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4767       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4768       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4769       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4770       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4771       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4772       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4773       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4774       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4775       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4776       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4777       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4778       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4779       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4780       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4781       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4782       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4783       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4784       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4785       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4786       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4787       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4788       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4789       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4790       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4791       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4792       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4793       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4794       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4795       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4796       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4797       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4798       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4799       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4800       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4801       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4802       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4803       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4804       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4805       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4806       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4807       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4808       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4809       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4810       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4811       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4812       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4813       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4814       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4815       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4816       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4817       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4818       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4819       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4820       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4821       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4822       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4823       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4824       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4825       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4826       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4827       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4828       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4829       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4830       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4831       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4832       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4833       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4834       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4835       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4836       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4837       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4838       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4839       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4840       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4841       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4842       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4843       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4844       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4845       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4846       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4847       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4848       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4849       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4850       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4851       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4852       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4853       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4854       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4855       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4856       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4857       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4858       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4859       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4860       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4861       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4862       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4863       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4864       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4865       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4866       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4867       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4868       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4869       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4870       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4871       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4872       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4873       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4874       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4875       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4876       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4877       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4878       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4879       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4880       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4881       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4882       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4883       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4884       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4885       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4886       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4887       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4888       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4889       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4890       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4891       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4892       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4893       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4894       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4895       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4896       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4897       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4898       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4899       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4900       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4901       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4902       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4903       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4904       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4905       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4906       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4907       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4908       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4909       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4910       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4911       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4912       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4913       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4914       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4915       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4916       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4917       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4918       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4919       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4920       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4921       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4922       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4923       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4924       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4925       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4926       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4927       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4928       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4929       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4930       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4931       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4932       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4933       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4934       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4935       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4936       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4937       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4938       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4939       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4940       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4941       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4942       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4943       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4944       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4945       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4946       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4947       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4948       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4949       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4950       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4951       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4952       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4953       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4954       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4955       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4956       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4957       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4958       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4959       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4960       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4961       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4962       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4963       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4964       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4965       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4966       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4967       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4968       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4969       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4970       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4971       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4972       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4973       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4974       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4975       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4976       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4977       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4978       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4979       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4980       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4981       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4982       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4983       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4984       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4985       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4986       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4987       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4988       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4989       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4990       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4991       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4992       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4993       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4994       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4995       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4996       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4997       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4998       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   4999       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5000       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5001       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5002       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5003       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5004       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5005       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5006       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5007       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5008       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5009       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5010       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5011       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5012       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5013       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5014       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5015       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5016       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5017       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5018       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5019       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5020       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5021       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5022       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5023       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5024       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5025       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5026       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5027       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5028       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5029       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5030       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5031       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5032       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5033       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5034       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5035       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5036       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5037       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5038       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5039       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5040       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5041       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5042       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5043       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5044       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5045       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5046       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5047       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5048       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5049       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5050       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5051       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5052       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5053       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5054       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5055       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5056       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5057       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5058       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5059       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5060       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5061       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5062       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5063       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5064       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5065       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5066       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5067       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5068       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5069       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5070       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5071       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5072       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5073       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5074       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5075       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5076       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5077       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5078       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5079       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5080       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5081       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5082       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5083       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5084       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5085       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5086       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5087       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5088       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5089       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5090       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5091       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5092       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5093       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5094       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5095       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5096       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5097       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5098       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5099       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5100       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5101       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5102       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5103       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5104       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5105       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5106       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5107       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5108       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5109       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5110       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5111       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5112       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5113       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5114       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5115       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5116       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5117       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5118       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5119       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5120       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5121       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5122       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5123       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5124       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5125       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5126       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5127       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5128       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5129       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5130       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5131       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5132       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5133       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5134       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5135       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5136       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5137       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5138       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5139       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5140       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5141       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5142       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5143       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5144       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5145       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5146       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5147       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5148       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5149       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5150       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5151       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5152       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5153       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5154       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5155       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5156       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5157       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5158       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5159       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5160       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5161       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5162       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5163       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5164       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5165       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5166       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5167       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5168       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5169       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5170       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5171       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5172       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5173       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5174       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5175       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5176       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5177       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5178       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5179       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5180       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5181       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5182       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5183       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5184       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5185       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5186       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5187       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5188       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5189       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5190       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5191       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5192       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5193       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5194       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5195       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5196       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5197       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5198       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5199       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5200       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5201       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5202       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5203       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5204       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5205       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5206       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5207       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5208       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5209       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5210       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5211       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5212       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5213       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5214       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5215       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5216       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5217       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5218       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5219       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5220       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5221       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5222       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5223       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5224       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5225       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5226       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5227       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5228       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5229       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5230       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5231       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5232       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5233       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5234       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5235       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5236       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5237       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5238       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5239       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5240       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5241       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5242       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5243       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5244       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5245       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5246       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5247       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5248       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5249       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5250       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5251       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5252       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5253       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5254       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5255       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5256       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5257       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5258       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5259       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5260       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5261       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5262       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##   5263       NA    NA    NA     NA    NA      NA     NA     NA           NA
    ##  [ reached getOption("max.print") -- omitted 331513 rows ]

\#1: There are 8255 flights that have a missing departure time. Other
variables that are missing from this data are the arrival times,
departure delay. These rows might represent the flights that were
cancelled or rescheduled.

\#2: Currently dep\_time and sched\_dep\_time are convenient to look at,
but hard to compute with because theyâ€™re not really continuous
numbers. Convert them to a more convenient representation of number of
minutes since midnight.

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.3     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.4     ✓ dplyr   1.0.4
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.4.0     ✓ forcats 0.5.0

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
b <- transmute(flights,
    dep_time,
    dep_time_minutes = (dep_time %/% 100)*60 + (dep_time %% 100))
c <- transmute(flights,
    sched_dep_time,
    sched_dep_time_minutes = (sched_dep_time %/% 100)*60 + (sched_dep_time %% 100))
mutate(b, c)
```

    ## # A tibble: 336,776 x 4
    ##    dep_time dep_time_minutes sched_dep_time sched_dep_time_minutes
    ##       <int>            <dbl>          <int>                  <dbl>
    ##  1      517              317            515                    315
    ##  2      533              333            529                    329
    ##  3      542              342            540                    340
    ##  4      544              344            545                    345
    ##  5      554              354            600                    360
    ##  6      554              354            558                    358
    ##  7      555              355            600                    360
    ##  8      557              357            600                    360
    ##  9      557              357            600                    360
    ## 10      558              358            600                    360
    ## # … with 336,766 more rows

\#3: Look at the number of cancelled flights per day. Is there a
pattern? Is the proportion of cancelled flights related to the average
delay? Use multiple dyplr operations, all on one line, concluding with
\`ggplot(aes(x= ,y=)) + geom\_point()’

``` r
flights %>% group_by(year, month, day) %>% summarise(n_fcancel = sum(is.na(air_time) | air_time == 0),avg_arr_delay = mean(arr_delay, na.rm = TRUE), avg_dep_delay = mean(dep_delay, na.rm = TRUE) ) %>%
select(year, month, day, n_fcancel, avg_arr_delay, avg_dep_delay) %>%
filter(avg_arr_delay > 0) %>% ggplot()+ geom_point(aes(x = avg_arr_delay, y = n_fcancel, color = "red"))+ geom_point(aes(x = avg_dep_delay, y = n_fcancel,color =  "blue")) 
```

    ## `summarise()` has grouped output by 'year', 'month'. You can override using the `.groups` argument.

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

The proportion of cancelled flights increases as the average delay time
increases.

github link:
