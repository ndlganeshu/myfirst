# myfirst
testing the github in my local


## React Router v6

1. Add react-router-dom@6.4.0 
2. created new file myRoutes.js with the below content
```
import {
  createBrowserRouter,
  Link,
} from "react-router-dom";
import About from './About'

const router = createBrowserRouter([
  {
    path: "/",
    element: (
      <div>
        <h1>Hello World</h1>
        <Link to="about">About Us</Link>
      </div>
    ),
  },
  {
    path: "about",
    element: <About />
  },
]);

export default router;
```
3. index.js add the RouteProvider as below
```
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import {
  RouterProvider
} from "react-router-dom";
import App from "./App";
import router from './myRoutes'

const rootElement = document.getElementById("root");
const root = createRoot(rootElement);

root.render(
  <StrictMode>
    <RouterProvider router={router} />
    <App />
  </StrictMode>
);
```
