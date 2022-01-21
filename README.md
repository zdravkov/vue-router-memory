A possible memory leak with Vue - vue router and lots ov rendered components
Steps:

npm i

npm run serve

We have two routes - one of them with 1000 components in it
start switching the routes fast and watch the memory increasing:
![memoryleak](https://user-images.githubusercontent.com/9494406/150487157-3c5fae75-488d-4b39-8617-9930af7f2f9f.gif)
