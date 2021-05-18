<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <script src="./lib/vue.js"></script>
</head>
<body>
    <div id="app">
        <my-component>hello1</my-component>
        <my-component>hello2</my-component>
        <my-component>hello3</my-component>
    </div>


    <template id="first">
        <div>
            <slot></slot>
        </div>
    </template>
    <script>
        Vue.component('my-component',{ template:'#first'})
        var vm =new Vue({
            el:'#app'
        })
    </script>
</body>
</html>
