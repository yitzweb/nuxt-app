Aug 10, 2022

contents in this folder from
https://developer.school/tutorials/create-your-first-nuxt-3-app-with-tailwind

I just finished adding the about page. I get following error when starting the server:

> $ npm run dev
> ERROR  Cannot start nuxt:  Cannot find module 'nuxt3'

Trying the solution here: https://github.com/nuxt/framework/discussions/3060

> For anyone with this problem - do the following to fix:
> Update package.json
> {
>   "devDependencies": {
> -    "nuxt3": "latest"
> +    "nuxt": "npm:nuxt3@latest"
>   }
> }
> Update nuxt.config:
> - import { defineNuxtConfig } from 'nuxt3'
> + import { defineNuxtConfig } from 'nuxt'
> 
> export default defineNuxtConfig({ ... })
> (optional, if it still isn't working):
> 
> Delete node_modules folder
> Delete package.lock.json if present
> Delete .nuxt and .output folders
> Rebuild by running npm install or yarn

I did that but I also had to add an index.vue file to the pages folder. I did that and it basically worked. Hoewver, there were many warnings in the log. This project seems to have been from 2021. It could be that there are errors in the code because it was from a Beta version of Nuxt 3. For now, I'm going to stop with this one and try to do a different tutorial.