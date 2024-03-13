# Set up react outside react environment with CDN 


### use CDN (Content Delivery Network)

~~~JS
 <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
 <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
~~~


### Live server extension 

Install live server from extensions

. To open Live server:  
ctrl+L + clt+O

. to close live server:  
ctrl+L +clt+C 


### ReactDOM library

 we insallled in the CDN, which has the global variable ReactDOM and render method to render our html on the element with the id we choose in index.html file.
 we append to the root id element this h1 element 

~~~JSX
index.js

ReactDOM.render(<h1>Hello, this is me!</h1>, document.getElementById("root"))

or 

ReactDOM.render(<h1>Hello there!</h1>, document.querySelector("#root") )
~~~

## Why react
- Because its <mark> composable </mark>
- 
~~~html
index.html

<body>
    <MyNavbar />
    <MyMainContent />
    <MyFooter />
</body>
~~~
~~~JSX
index.js

function Navbar(){
    return (
        <nav>
        <a>Navbar</a>
        ..
        </nav>
    )
}

ReactDOM.render(
    <div>
    <Navbar />
    </div>,
    document.getElementById("root")
)
~~~


- Becaude its <mark>declarative</mark>

  - ( declarative : what should be done ) 
  ~~~JSX
  ReactDOM.render(<h1 className="header">This is a declarative way of programming with JSX</h1>, document.getElementById("root"))

  ~~~
  - ( imperative : How should it be done )
  ~~~javascript
  const h1 = document.createElement("h1")
  h1.textContent = "This is an imperative way to program with vanilla JS"
  h1.className = "header"
  document.getElementById("root").append(h1)
  ~~~

## JSX
- We have to wrap all html elements in only one html element 
~~~JSX
const navbar = (
    <nav>
       <h1>Rita Restaurant</h1>
       <ul>
         <li>Menu</li>
         <li>About</li>
         <li>Contact</li>
       </ul>
    </nav>
)
reactDOM.render(nav, document.getElementById("root"))

or

reactDOM.render(  
    <nav>
       <h1>Rita Restaurant</h1>
       <ul>
         <li>Menu</li>
         <li>About</li>
         <li>Contact</li>
       </ul>
    </nav>,
     document.getElementById("root")
)
~~~

- It returns an object
  

# Deploy React project sat up with CDN on netlify
* Sign up to [Netflify](https://www.netlify.com/)
* Go to get started page
* Drag and Drop this project folder
* Celebrate 🎉

