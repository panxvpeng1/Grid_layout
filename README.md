# Grid_layout

//grid-template-columns和grid-template-rows分别表示垂直方向上item的宽和水平方向上item的高
```
.contain{
    display: grid;
    grid-template-columns:200px 200px 200px;
    grid-template-rows:200px 200px 200px;
    text-align: center;  
    /* 尽可能填满 */
    grid-auto-flow: row ;
}
```

//grid-template-areas配合grid-area实现
```
.contain{
    display: grid;
    /* auto */
    grid-template-columns: 200px 200px 200px ;
    grid-template-rows: 200px 200px 200px 200px;
    grid-template-areas:"h h h"
                        "n . m"
                        "n . m"
                        "f f f";
}
.contain .h{
    grid-area:h ;
    background-color: gray;
}
.contain .n{
    grid-area:n ;
    background-color: green;
}
.contain .m{
    grid-area:m ;
    background-color: greenyellow;
}
.contain .f{
    grid-area:f ;
    background-color: indianred;
}
```

//grid-column-gap和grid-row-gap表示每个item竖直方向和水平方向上的间隙
```
.contain{
    display: grid;
    /* auto */
    grid-template-columns: 200px 200px 200px ;
    grid-template-rows: 200px 200px 200px;
    grid-column-gap: 10px;
    grid-row-gap: 10px;
}
```
//grid-auto-rows设置不在设置范围内的item的高
```
.contain{
    display: grid;
    grid-template-columns:200px 200px 200px;
    grid-template-rows:200px 200px 200px;
    text-align: center;  
    /* 超出部分高度50px */
    grid-auto-rows: 50px;
}
```


//grid-auto-flow设置item的排列方式如：水平从左到右 从上到下 还可以设置是否尽量占满
```
.contain{
    display: grid;
    grid-template-columns:200px 200px 200px;
    grid-template-rows:200px 200px 200px;
    text-align: center;  
    grid-auto-flow: column dense;
}
```
//repeat第一个参数重复次数 后面的参数表示被重复的组
```
.contain{
    display: grid;
    grid-template-columns:repeat(2,200px 50px 100px);
    text-align: center;  
}
```
//minmax最小最大值
```
.contain{
    display: grid;
    grid-template-columns: 1fr 1fr minmax(500px, 1fr);
}
```
//place-items 传入两个参数表示justify-items align-items的值
```
.contain{
    display: grid;
    grid-template-columns:1fr 1fr 1fr;
    /*  justify-items: start | end | center | stretch;
        align-items: start | end | center | stretch; */         
    /* justify-items: center;
    align-items: center; */
    place-items: center center;
}
```
//place-content 传入两个参数表示justify-content align-content
```
.contain{
    height: 600px;
    width: 900px;
    border: 1px solid #000;
    display: grid;
    grid-template-columns:200px 200px 200px;
    /*  justify-content:center;
        align-content:center; */
    place-content: center center;
}
```
//fr表示一个比例关系
```
.contain{
    display: grid;
    grid-template-columns:1fr 200px 1fr;   
}
```

//auto自动填满
```
.contain{
    display: grid;
    grid-template-columns: 200px auto 100px ;
}
```
//auto-fill自动设置重复次数尽量沾满一行
```
.contain{
    display: grid;
    /* auto-fill */
    grid-template-columns:repeat(auto-fill,200px);
    text-align: center;  
}
```
