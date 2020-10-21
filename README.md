@kjbrum 
I tried different combination of z-indexes of 10000 and -1 and i felt kinda stupid.\
I think the problem is - as i read [here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context)
, when i hover over the parent element and apply transform to it - it creates a new stacking context, where z-indexes don't matter anymore.\
I thought maybe adding some features or properties could resolve the  issue:
like (will-change: transform, ) or different layout.\
So far i don't see what it is.\\
I don't know, maybe you could remember - when you were creating this effect: you put two cards aka ```::before``` and ```::after``` below the parent card and when  you hover over do this:
```
 &:hover {
        transform: translate(-5px, 0);
        
        &:before { transform: translate(5px, 0) scale(0.95); }
        &:after { transform: translate(10px, 0) scale(0.90); }
    }
```
Is there anything else needed just to translate cards?
Like maybe i don't get smth important about it.
I thought this effect would be easy, but that cards are telling me no.
[here] (https://jsfiddle.net/tfwkbme4/12/) i tried once more,  but it just bullies me again.
