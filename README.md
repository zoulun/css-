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
            width: 200px;
            background-color: #377159;
        }
        .float .right {
            width: 200px;
            float: right;
            background-color: #b7bb92;
        }
        .float .main {
            background-color: #5a6c80;
        }
    </style>
    <article>
        <h1>float</h1>
        <div class="container float">
            <div class="left"></div>
            <div class="right"></div>
            <div class="main">float</div>
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
            background-color: #377159;
        }
        .position .right {
            right: 0;
            width: 200px;
            background-color: #b7bb92;
        }
        .position .main {
            left: 200px;
            right: 200px;
            background-color: #5a6c80;
        }
    </style>
    <article>
        <h1>BFC</h1>
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
            background-color: #377159;
        }
        .flex .right {
            width: 200px;
            background-color: #b7bb92;
        }
        .flex .main {
            flex: 1;
            background-color: #5a6c80;
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
            background-color: #377159;
        }
        .table .right {
            width: 200px;
            background-color: #b7bb92;
        }
        .table .main {
            background-color: #5a6c80;
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
            background-color: #377159;
        }
        .grid .right {
            background-color: #b7bb92;
        }
        .grid .main {
            background-color: #5a6c80;
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
