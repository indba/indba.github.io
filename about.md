---
layout: page
title: Graphs
---

* Gravizo Online
'''
![Alt text](http://g.gravizo.com/g?
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf};
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
)
'''

* Graphviz-Plugin

{% xneato svg %}    
digraph TrafficLights {
node [shape=box];  gy2; yr2; rg2; gy1; yr1; rg1;
node [shape=circle,fixedsize=true,width=0.9];  green2; yellow2; red2; safe2; safe1; green1; yellow1; red1;
gy2->yellow2;
rg2->green2;
yr2->safe1;
yr2->red2;
safe2->rg2;
green2->gy2;
yellow2->yr2;
red2->rg2;
gy1->yellow1;
rg1->green1;
yr1->safe2;
yr1->red1;
safe1->rg1;
green1->gy1;
yellow1->yr1;
red1->rg1;

overlap=false
label="PetriNet Model TrafficLights\nExtracted from ConceptBase and layed out by Graphviz"
fontsize=12;
}
{% endxneato %}