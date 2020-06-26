# Template customization


## public
I hope you have seen this template `public` folder on the downloaded package `Sapp - Vue JS App Landing Page` from ThemeForest.

In this `public` folder you can see `index.html` file. This file structure is like this-

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!--meta, title, google fonts, all css linking here-->
</head>

<body>

  <div id="app"></div>
 
 <!--all js linking here-->
</body>

</html>
```

All HTML content will be load into this `div`:
```html
<div id="app"></div>
```


## entry points

##### main.js
Template `main.js` structure looks like this-
```js
import Vue from 'vue'
import App from './App.vue'
import router from './router'

Vue.config.productionTip = false

new Vue({
  router,
  render: h => h(App),
}).$mount('#app')

```

##### app.vue
Template `app.vue` structure looks like this-
```vue
<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>

```


## themes

`themes` folder included on `src` folder. You can check our folder structure on `src` folder menu.
This is `theme` folder structure-
```text
|-- themes
    |-- theme-one.vue ( default theme)
    |-- theme-two.vue ( demo theme 2)
    .....
    |-- theme-six.vue ( demo theme 6 )
```

`theme` folder contains all of our 6 demos.


## routes
In `router` folder we used `index.js`. Where we linked all the route for our all theme. For routing we used vue-router.

Routes: `router/index.js`

```js
import Vue from 'vue'
import Router from 'vue-router'
import ThemeOne from '@/themes/theme-one'
import ThemeTwo from '@/themes/theme-two'
import ThemeThree from '@/themes/theme-three'
import ThemeFour from '@/themes/theme-four'
import ThemeFive from '@/themes/theme-five'
import ThemeSix from '@/themes/theme-six'
import Pricing from '@/components/InnerPages/PricingPage/pricing'
import Download from '@/components/InnerPages/DownloadPage/download'
import Newsletter from '@/components/InnerPages/NewsletterPage/newsletter'
import ThankYou from '@/components/InnerPages/ThankYou/thankyou'
import ComingSoon from '@/components/InnerPages/ComingSoon/coming-soon'
import Error from '@/components/InnerPages/Error/404'
import BlogTwoColumn from '@/components/Blogs/BlogTwoColumn/blog-two-column'
import BlogThreeColumn from '@/components/Blogs/BlogThreeColumn/blog-three-column'
import BlogLeftSidebar from '@/components/Blogs/BlogLeftSidebar/blog-left-sidebar'
import BlogRightSidebar from '@/components/Blogs/BlogRightSidebar/blog-right-sidebar'
import BlogDetailsLeftSidebar from '@/components/Blogs/BlogDetailsLeftSidebar/blog-details-left-sidebar'
import BlogDetailsRightSidebar from '@/components/Blogs/BlogDetailsRightSidebar/blog-details-right-sidebar'
import Login from '@/components/Accounts/Login/login'
import SignUp from '@/components/Accounts/SignUp/signup'
import Forgot from '@/components/Accounts/Forgot/forgot'
import Reviews from '@/components/InnerPages/ReviewPage/reviews'
import Faq from '@/components/InnerPages/FaqPage/faq'
import Contact from '@/components/InnerPages/ContactPage/contact'

Vue.use(Router)

export default new Router({
  mode: 'history',
  routes: [
    {
      path: '/',
      name: 'ThemeOne',
      component: ThemeOne
    },
    {
      path: '/theme-two',
      name: 'ThemeTwo',
      component: ThemeTwo
    },
    {
      path: '/theme-three',
      name: 'ThemeThree',
      component: ThemeThree
    },
    {
      path: '/theme-four',
      name: 'ThemeFour',
      component: ThemeFour
    },
    {
      path: '/theme-five',
      name: 'ThemeFive',
      component: ThemeFive
    },
    {
      path: '/theme-six',
      name: 'ThemeSix',
      component: ThemeSix
    },
    {
      path: '/pricing',
      name: 'Pricing',
      component: Pricing
    },
    {
      path: '/download',
      name: 'Download',
      component: Download
    },
    {
      path: '/newsletter',
      name: 'Newsletter',
      component: Newsletter
    },
    {
      path: '/thankyou',
      name: 'ThankYou',
      component: ThankYou
    },
    {
      path: '/coming-soon',
      name: 'ComingSoon',
      component: ComingSoon
    },
    {
      path: '/404',
      name: 'Error',
      component: Error
    },
    {
      path: '/blog-two-column',
      name: 'BlogTwoColumn',
      component: BlogTwoColumn
    },
    {
      path: '/blog-three-column',
      name: 'BlogThreeColumn',
      component: BlogThreeColumn
    },
    {
      path: '/blog-left-sidebar',
      name: 'BlogLeftSidebar',
      component: BlogLeftSidebar
    },
    {
      path: '/blog-right-sidebar',
      name: 'BlogRightSidebar',
      component: BlogRightSidebar
    },
    {
      path: '/blog-details-left-sidebar',
      name: 'BlogDetailsLeftSidebar',
      component: BlogDetailsLeftSidebar
    },
    {
      path: '/blog-details-right-sidebar',
      name: 'BlogDetailsRightSidebar',
      component: BlogDetailsRightSidebar
    },
    {
      path: '/login',
      name: 'Login',
      component: Login
    },
    {
      path: '/signup',
      name: 'SignUp',
      component: SignUp
    },
    {
      path: '/forgot',
      name: 'Forgot',
      component: Forgot
    },
    {
      path: '/reviews',
      name: 'Reviews',
      component: Reviews
    },
    {
      path: '/faq',
      name: 'Faq',
      component: Faq
    },
    {
      path: '/contact',
      name: 'Contact',
      component: Contact
    }
  ]
})

```


## components
Under `components` folder we wrote all of our components individually. 
We have written these components to make the developer’s life easy. 
By using these basic components, For example in our components directory there is `HeaderSection`, `HeroSection` , `FooterSection` folder where we wrote our different styled component. For example `HeroSection` component-

### Component folder structure
```text
|-- components
    ....
    |-- HeroSection ( hero component folder )
        - heroOne.vue ( main demo hero section )
        - heroTwo.vue ( demo two hero section )
        ...... ( and other )
        
    |-- ContactSection ( contact folder )
        - contactOne.vue 
        - contactTwo.vue
        - contactThree.vue
    .
    ..
    ...    
```

### Contact Section component
`ContactSection/contactOne.vue`
```vue
<template>
    <section id="contact" class="contact-area bg-gray ptb_100">
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-12 col-md-10 col-lg-6">
                        <!-- Section Heading -->
                        <div class="section-heading text-center">
                            <h2 class="text-capitalize">Stay Tuned</h2>
                            <p class="d-none d-sm-block mt-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum obcaecati dignissimos quae quo ad iste ipsum officiis deleniti asperiores sit.</p>
                            <p class="d-block d-sm-none mt-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum obcaecati.</p>
                        </div>
                    </div>
                </div>
                <div class="row justify-content-between">
                    <div class="col-12 col-md-5">
                        <!-- Contact Us -->
                        <div class="contact-us">
                            <p class="mb-3">Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.</p>
                            <ul>
                                <li class="py-2">
                                    <a class="media" href="#">
                                        <div class="social-icon mr-3">
                                            <i class="fas fa-home"></i>
                                        </div>
                                        <span class="media-body align-self-center">Vestibulum nulla libero, convallis, tincidunt suscipit diam, DC 2002</span>
                                    </a>
                                </li>
                                <li class="py-2">
                                    <a class="media" href="#">
                                        <div class="social-icon mr-3">
                                            <i class="fas fa-phone-alt"></i>
                                        </div>
                                        <span class="media-body align-self-center">+1 230 456 789-012 345 6789</span>
                                    </a>
                                </li>
                                <li class="py-2">
                                    <a class="media" href="#">
                                        <div class="social-icon mr-3">
                                            <i class="fas fa-envelope"></i>
                                        </div>
                                        <span class="media-body align-self-center">exampledomain@domain.com</span>
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 pt-4 pt-md-0">
                        <!-- Contact Box -->
                        <div class="contact-box text-center">
                            <!-- Contact Form -->
                            <form id="contact-form" method="POST" action="assets/php/mail.php">
                                <div class="row">
                                    <div class="col-12">
                                        <div class="form-group">
                                            <input type="text" class="form-control" name="name" placeholder="Name" required="required">
                                        </div>
                                        <div class="form-group">
                                            <input type="email" class="form-control" name="email" placeholder="Email" required="required">
                                        </div>
                                        <div class="form-group">
                                            <input type="text" class="form-control" name="subject" placeholder="Subject" required="required">
                                        </div>
                                    </div>
                                    <div class="col-12">
                                        <div class="form-group">
                                            <textarea class="form-control" name="message" placeholder="Message" required="required"></textarea>
                                        </div>
                                    </div>
                                    <div class="col-12">
                                        <button type="submit" class="btn btn-lg btn-block mt-3"><span class="text-white pr-3"><i class="fas fa-paper-plane"></i></span>Send Message</button>
                                    </div>
                                </div>
                            </form>
                            <p class="form-message"></p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
</template>

<script>
export default {
    
}
</script>

<style>

</style>
```

## theme installtion
To install the theme you have to install [vue](https://cli.vuejs.org/) than go to the theme root dir where `package.json` located and use
```bash
npm install
```
it will install the packages.

After install process now you can run local server- local server port is 'http://localhost:8080' For developement start use
```bash
npm run serve
```
## Build your theme
```bash
npm run build
```

## For deployment -- static server
First install
```bash
npm install -g serve
serve -s build
```
If you want to know more about static deployment please visit [Create vue app deployment](https://cli.vuejs.org/guide/deployment)

Enjoy your theme :)
