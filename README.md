# css三栏布局的五种方法
```html
<section>
    <style>
        .float:after{
            content: '';
            display: block;
            clear: both;
        }
        .float .left {
            float: left;
            width: 100px;
            background-color: red;
        }
        .float .right {
            width: 100px;
            float: right;
            background-color: blue;
        }
        .float .main {
            background-color: green;
        }
    </style>
    <article>
        <h1>浮动</h1>
        <div class="container float">
            <div class="left"></div>
            <div class="right"></div>
            <div class="main">深Vvvv</div>
        </div>
    </article>
</section>
    <section>
        <style>
            .position{
                position: relative;
            }
            .position>div{
                position: absolute;
            }
            .position .left {
                left: 0;
                width: 200px;
                background-color: red;
            }
            .position .right {
                right: 0;
                width: 200px;
                background-color: blue;
            }
            .position .main {
                left: 200px;
                right: 200px;
                background-color: green;
            }
        </style>
        <article>
            #<h1>BFC</h1>
            <div class="container position">
                <div class="left"></div>
                <div class="right"></div>
                <div class="main">position</div>
            </div>
        </article>
    </section>
<section>
    <style>
        .flex-container{
            margin-top: 200px;
        }
        .flex{
            display: flex;
        }
        .flex .left {
            width: 200px;
            background-color: red;
        }
        .flex .right {
            width: 200px;
            background-color: blue;
        }
        .flex .main {
            flex: 1;
            background-color: green;
        }
    </style>
    <article class="flex-container">
        <h1>flex</h1>
        <div class="container flex">
            <div class="left"></div>
            <div class="main">flex</div>
            <div class="right"></div>
        </div>
    </article>
</section>
<section>
    <style>
        .table{
            width: 100%;
            display: table;
        }
        .table .left,.table .right,.table .main{
            display: table-cell;
        }
        .table .left{
            width: 200px;
            background-color: red;
        }
        .table .right {
            width: 200px;
            background-color: blue;
        }
        .table .main {
            background-color: green;
        }
    </style>
    <article>
        <h1>table</h1>
        <div class="container table">
            <div class="left"></div>
            <div class="main">table</div>
            <div class="right"></div>
        </div>
    </article>
</section>
<section>
    <style>
        .grid{
            width: 100%;
            display: grid;
            grid-template-rows: 100px;
            grid-template-columns: 200px auto 200px;
        }
        .grid .left{
            background-color: red;
        }
        .grid .right {
            background-color: blue;
        }
        .grid .main {
            background-color: green;
        }
    </style>
    <article>
        <h1>grid</h1>
        <div class="container grid">
            <div class="left"></div>
            <div class="main">grid</div>
            <div class="right"></div>
        </div>
    </article>
</section>
```
