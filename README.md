# Vue Hamlet
vue-hamlet is used as authentication for frontend.

## Index
* [Install](#install)
* [Demo](#demo)
* [TODO](#white_check_mark-todo)
* [Configuration](#configuration)

## Install
Install repository into your project.
~~~
> npm install yimian/vue-hamlet --save-dev
~~~
Configure setting in your project main.js
~~~
import VueResource from 'vue-resource';
import { sync } from 'vuex-router-sync';
import auth from 'vue-hamlet';
import router from './router';
import store from './store';

Vue.use(VueResource);
Vue.store = store;
Vue.router = router;

Vue.use(auth, {
  fetchUser: '',
  appKey: '',
});

sync(store, router);
~~~

## :white_check_mark: TODO
- :heavy_check_mark: mod: change VueResource to axios.

## Demo
Run demo project with following procedures:
~~~
cd demo/
~~~
~~~
npm install
~~~
~~~
npm run dev
~~~


## Configuration
Default Configuration:
~~~
fetchUser: '/api/auth/me',
appKey: '',
authType: 'Bearer',
hamletPrefix: '/api/auth',
authRedirect: '/login',
refreshInterval: 10, // mins
forbiddenRedirect: '/403',
notFoundRedirect: '/404',
~~~

You can rewrite default configuration in your project like:
~~~
Vue.use(auth, {
  appKey: '',
});
~~~
