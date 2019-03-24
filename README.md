# Parcel
Trying Parcel after licking some Webpack.   



## Experience with Webpack (v4)
So while I get the idea behind loaders, it's hard for me to understand how the plugins work, how they are attached and get the data. While it works, I don't feel comfortable using it. Then there are hundreds of loaders, configurations, and thousands of community-created plugins. I've used it only for one time and felt very overwhelmed by it. I followed the official docs guide and many things are not clear for me. I'm sure however that after 2 weeks of playing with it all day, I would get comfortable, and maybe I will, if Parcel doesn't fulfill my requirements, which basically aren't that high so I think Webpack is overkill.



## What do I Need?
Basically, I want to have 2 directories - `src/` and `build/`.   
I write code only in the `src/` directory and the `build/` is for production-ready, minified etc. HTML, CSS and JS.   
### JavaScript
- Bundle ES6 modules
- Transpile ES6+ to ES5
- Minify ES5

### CSS
- Transpile Sass to CSS
- Autoprefix CSS
- Minify CSS

### HTML
- Minify HTML

That's all I want, that's all I need. Can Parcel do it? I hope so. Let's find out!



## Website - First Impression
First, I like [Parcel's website](https://en.parceljs.org/).   
It is simple, minimalistic, clean and very easy to scan. Love it.   
Additionaly, it supports 12 languages while Webpack supports 2.   
But it's not about the website, it's about the bundler, right? Let's go.



## What is Parcel?
"Blazing fast, zero configuration web application bundler" - sounds good.

### Features

#### Blazing Fast Bundle Times
"Parcel uses worker processes to enable multicore compilation, and has a filesystem cache for fast rebuilds even after a restart."

#### Bundle all the Assets, Out of the Box
"Parcel has out of the box support for JS, CSS, HTML, file assets, and more - no plugins needed." - Yeah! No more confusing Webpack plugins!

#### Automatic Transforms
"Code is automatically transformed using Babel, PostCSS, and PostHTML when needed - even node_modules." - Love it!

#### Zero Config Code Splitting
"Using the dynamic import() syntax, Parcel splits your output bundles so you only load what is needed on initial load."

#### Hot Module Replacement
"Parcel automatically updates modules in the browser as you make changes during development, no configuration needed."

#### Friendly Error Logging
"Parcel prints syntax highlighted code frames when it encounters errors to help you pinpoint the problem."

### Bonus: Interesting Benchmark
This is not my benchmark, it's from their official website.   
The benchmark was based on reasonably sized app containing 1726 modules, 6.5MB uncompressed, and built on a 2016 MacBook Pro with 4 physical cores.   
Here are the results:   
- Browserify: 22.98s
- Webpack: 20.71s
- Parcel: 9.98s
- Parcel with cache: 2.64s



## Installation
Enought theory. Let's see how it performs in real life projects. Install it with:   
```
npm install -g parcel-bundler
```



## The Project
So, I'll create a todo app to see if Parcel can fulfill the requirements I placed above.   

### 1. Initialize npm
Beginnings aren't always hard: `npm init -y`. Adjust the `package.json` if you want.