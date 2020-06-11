
# install PHP >= 7.2.5
# install PHP libs BCMath, Ctype, Fileinfo, JSON, Mbstring, OpenSSL, PDO, Tokenizer, XML
# install composer
# install git
# install node
# install npm
# install yarn
# npm install -g @vue/cli


mkdir app
cd app

composer create-project --prefer-dist laravel/laravel .

git init

git add .

git commit -m "first commit"

composer require laravel/ui

php artisan ui vue
#php artisan ui vue --auth

npm install

git add .

git commit -m "add vue"

npm install ts-loader typescript --save-dev

node_modules/.bin/tsc --init

# https://sebastiandedeyne.com/typescript-with-laravel-mix/
# https://medium.com/@titasgailius/initial-laravel-setup-with-vuejs-vue-router-vuex-in-typescript-305f7fe9d62b

git add .

git commit -m "install typescript"

npm install vue-class-component vue-property-decorator

git add .

git commit -m "install lib vue-typescript"

git mv resources/js/app.js resources/js/app.ts
git mv resources/js/bootstrap.js resources/js/bootstrap.ts
git commit -m "change extension"

change webpack.mix.js
    mix.js('resources/js/app.js', 'public/js')
        by
            mix.ts('resources/js/app.ts', 'public/js')

change resources/js/app.ts
change resources/js/bootstrap.ts

touch resources/js/typings.d.ts
change resources/js/typings.d.ts

change resources\js\components\ExampleComponent.vue
    <script lang="ts">
        import Vue from "vue"
        import Component from "vue-class-component"

        @Component
        export default class ExampleComponent extends Vue {
            //
        }
    </script>
