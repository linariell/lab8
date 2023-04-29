<p></p>

<h2 align="center">ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ <br> «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ» <br> КАФЕДРА ИНФОРМАТИКИ </h2>
<p align="center">Лабораторная работа №8 <br>
по курсу «Web-технологии, языки и средства создания web-приложений» 

<p align="center"><b>"Java Script"</b><p>
<p align="right"><b>Выполнила: </b> студентка 231 группы Витковская Полина</p>
<p  align="right"><b>Принял: </b> Соболев Е. И., старший преподователь</p>
<br>
<br>
<br>
<p align="center">Южно-Сахалинск <br> СахГУ <br> 2023</p>
<h2> Введение </h2>
<p>Лабораторные работы по дисциплине «Web-технологии, языки и средства создания web-приложений» предназначены для освоения полученных теоретических знаний на практике. Перед началом первой лабораторной работы были поставлены цели: <br>
<ol>
  <li>Овладеть навыками работы с языком гипертекстовой разметки HTML, в частности научиться основам Java Script, создаватьскрипты для решения задач.
</ol>
В соответствии с данными целями необходимо решить следующие задачи:
<ol>
   <li> Написать скрипты для решения данных задач.
   </ol>
Для реализации данной работы будет использоваться Visual Studio Code. Выполнение кода будет происходить в браузере Google Chrome.
</p>
<h2>Решение задач</h2>
<p>На первой странице были выполнены первые 20 коротких задачи: </p>
<code>
    <script>
    //1
    if (true) console.log(1);
    if(false) console.log(2);
    //2
    let m,n;
    m=Math.floor(Math.random()*100);
    console.log("m="+m);
    if(m>50) {n="big";}
    else {n="small";}
    console.log(n);
    //3
    console.log("ответ:8")
    //4

    let i=45;
    while(i<68)
    {console.log(i++)}
    //5
    let a=45;
    while (a<=670)
    {
        if(a%10==0) {console.log(a);}
        a++;
    }
    //6
    for (let i=45;i<68;i++)
    {console.log(i);}
    for(let i=45;i<=670;i++)
    {
        if(i%10==0) {console.log(i);}
    }
    //7
    let num=Math.floor(Math.random()*3);
    console.log(num);
    switch(num) 
    {
        case 0:console.log("ноль"); break;
        case 1:console.log("один"); break;
        case 2:console.log("два"); break;
        case 3: console.log("три"); break;
    }
    //8
    for (let i=0;i<=10;i++)
    {document.write('<img src=url(https://avatars.dzeninfra.ru/get-zen_doc/34175/pub_5cea2361585c2f00b5c9cb0b_5cea310a752e5b00b25b9c01/scale_1200)>')}
    //9
    let size=120;
    let unit="Кб";

    switch (unit)
    {
        case "Кб":console.log(size*1024);break;
        case "Мб":console.log(size*1024*1024);break;
        case "Гб":console.log(size*1024*1024*1024);break;
    }
    //10
    let mounth=4;
    let table = '<table><tr><th>пн</th><th>вт</th><th>ср</th><th>чт</th><th>пт</th><th>сб</th><th>вс</th></tr><tr>';
        for (let i = 0; i < 5; i++) {
            table += '<td></td>';
        }
    for(let i=1;i<=30;i++)
            {
                table+='<td>' + i + '</td>';
                if(i==2|i==9|i==16|i==23|i==30) {table += '</tr><tr>';}
            }

        table += '</tr></table>';

    calendar.innerHTML = table;
    //11
    function hello1() {return "Привет, js!"}
    console.log(hello1());
    //12
    function hello2(name) 
    {
        if(name !=null) {return "привет, "+name;}
        else return "привет, гость";
    }
    console.log(hello2("Полина"));
    console.log(hello2());
    //13
    function mul(x,y)
    {return x*y}
    console.log(mul(5,2));
    //14
    function repeat(str,n)
    {
        
        for(let i=1;i<n;i++)
        {str+=str;}
        return str;
    }
    console.log(repeat("meow",2))
    //15
    function rgb(r,g,b)
    {
        let a,d,c;
        if (r!=null) {a=r;} else {a=0;}
        if (g!=null) {d=g;} else {d=0;}
        if (b!=null) {c=b;} else {c=0;}
        return "rgb("+a+","+d+","+c+")"
    }
    console.log(rgb(1,2));
    //16
    function abg() 
    {
        let S=0;
        let i=0;
        while (arguments[i]!=null)
        {
            S+=arguments[i];
            i++;
        }
        return(S/i);
    }
    console.log(abg(2,3,1,8));
    //17
    function m1(a, b)
    {
        return mul(a, b);
    }
    
    function mul(a, b)
    {
        return a*b;
    }
    
    console.log(m1(8, 4));
    //18
    function operation(m,n,o)
    {
        switch (o)
        {
            case '+':return(m+n);break;
            case '-':return(m-n);break;
            case '/':return(m/n);break;
            case '*':return(m*n);break;
            default: return "error";break;
        }
    }
    console.log(operation(8, 4,'*'));
    //19
    function addN(n) {
        return function (b) {
            return n + b;
        };
    }
    //20
    function words(n)
    {
        if(n<9||n>19)
        {
            if (n%100/10==1) {return n+" Товаров";}
            if (n%10==1) {return n+" Товар";}
            if (n%10==2 || n%10==3 || n%10==4) {return n+" Товарa";}
            return n+" Товаров";
        } 
        else return n+" товаров"
    }
    console.log(words(12));
    console.log(words(22));
    </script>
</code>
<p>На второй странице были выполнены задачи с ресурса codewars.com:</p>
<code>

</code>
<h2>Вывод</h2>
<p>В ходе лабораторной работы были изучены элементы языка Java script. Были рассмотрены способы задания переменных, операций над ними, была проведена работа с циклами и функциями. Результатом лабораторной работы является два сайта с решенными задачами.</p>
