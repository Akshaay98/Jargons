 # 1)WTF are Babel and Webpack 😵 ? Explained in 2 mins. #
Babel
Babel is simply a translator, who translates your 'fancy' (ES6+) JS code into 'not-so-fancy' (ES5) ones that browser (front-end) or Node.js (back-end) understands.

Why we speak fancier than browser and Node.js? Because we can't wait to use the latest and greatest, even before they are officially supported.

Webpack
If Babel is a translator for JS, you can think of Webpack as a mega-multi-translator that works with all kinds of languages (or assets). For example, Webpack often runs Babel as one of its jobs. Another example, Webpack can collect all your inline CSS styles in your Javascript files and bundle them into one.

Why do we need such a monster for front-end, but not back-end?

Because front-end has many kinds of assets such as CSS, SASS, images, fonts and is way more complex and dynamic than back-end which only has JS. And in the end of day we need to somehow package all variety of assets into a small file that our users' browser can download at page load time. This is also known as minify and uglify. You see, back-end has none of the above requirement.

Another important reason is that front-end doesn't work with modules (again, in most cases). Modules are built-in features of Node.js, not browsers. Nowadays developers are so used to npm install, import and export JS modules in front-end, as it allows us to better organize code and share packages. But in reality they are only syntactic sugars, and it's Webpack's job to figure out all the dependencies among all the modules that we use in the code, and compile them into one big chunk of JS code that the browser actually understands.

When do we use Webpack in back-end? A good use case is to support SSR (Server-Side Rendering).

To sum up,
Backend: we use Babel so that we can use the fanciest JS syntax (ES6/7) with Node.js.
Frontend: we use Webpack (which uses Babel and other things) to compile JS code and many other assets into a few small bundle files that our users can download when they first load our webpage. For example, create-react-app uses Webpack and Babel when creating your app.

# Code-splitting in React (React.Lazy)  #
Normally, when the application compiles and runs, our code is bundled into a single javascript file that is passed to the browser, but as our application grows, the bundle gets very heavy in size and cumbersome. It directly hampers the performance of the application as loading such a heavy file on initial load takes too much time, thus making our application slow.

So, here comes React.lazy() to the rescue!

React.lazy() performs lazy loading through Code Splitting. Here, code splitting means that our code is now not bundled in a single file, rather it is divided into smaller chunks (javascript files), and each chunk is loaded lazily, that is, as and when required.
https://blog.logrocket.com/lazy-loading-components-in-react-16-6-6cea535c0b52/
With the advent of ES modules, transpilers such as Babel, and bundlers such as webpack and Browserify, you can now write JavaScript applications in a completely modular pattern for easy maintainability. Usually, each module is imported and merged into a single file called a bundle, then the bundle is included on a webpage to load the entire app. As the app grows, the bundle size increases and eventually impacts page load times.

Code-splitting is the process of dividing a large bundle of code into multiple bundles that can be loaded dynamically. This helps you avoid performance issues associated with oversized bundles without actually reducing the amount of code in your app.
With the advent of ES modules, transpilers such as Babel, and bundlers such as webpack and Browserify, you can now write JavaScript applications in a completely modular pattern for easy maintainability. Usually, each module is imported and merged into a single file called a bundle, then the bundle is included on a webpage to load the entire app. As the app grows, the bundle size increases and eventually impacts page load times.

Code-splitting is the process of dividing a large bundle of code into multiple bundles that can be loaded dynamically. This helps you avoid performance issues associated with oversized bundles without actually reducing the amount of code in your app.

React.lazy() makes it easy to create components that are loaded using dynamic import() but rendered like regular components. This automatically causes the bundle containing the component to load when the component is rendered.

React.lazy() takes as its argument a function that must return a promise by calling import() to load the component. The returned promise resolves to a module with a default export containing the React component.
When webpack sees this syntax, it knows to dynamically create a separate bundle file for the moment library.
# statement,expression,functional statement vs fuctional expression
https://medium.com/launch-school/javascript-expressions-and-statements-4d32ac9c0e74
