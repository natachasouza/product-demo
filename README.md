# product-demo
This Is the Base Repository of our Product App. As a developer of this team, you should start here by getting an overview of the technologies we use/plan to use in the future. This guide should also explain our choices and point you to other repositories you might need next. Ready to start?

# Technology Stack Choice #

This is a short guide on the stack of technologies we use and why. This covers both front and back-end, and also any external APIs and/or enablers we might use. There's also mention to some key points we've considered to the future, when we'll be scaling up the app.

## Front-End ##

There's no secret here. HTML + CSS + JavaScript. No need for reinventing the wheel, some of the best developer minds out there already said this is the best stack for Front-End App Development. In the next topics, you can read more about frameworks/libraries we use on the Front and why.

### HTML ###

<!DOCTYPE html>
Just plain HTML here, no libraries :books: needed. 

### CSS ###

Why writing 327 times in my stylesheet that my theme color is #4169E1? Why not just create a variable theme-color-blue: #4169E1 and use it everywhere? We should be focusing in accomplishing more by writing less!

The use of variables, nested rules and other advantages are the reasons why we're using preprocessors at our Product App.

There was some short discussion between using SCSS or SASS as preprocessor, but we ended up chosing SASS since the jump from SCSS to SASS isn't that big and SASS is more commonly used by the industry, which is a big advantage since it has a wider community (which means more support). 

If this is new to you, please check [SASS Documentation](https://sass-lang.com/documentation/file.SASS_REFERENCE.html) 

### JavaScript ###

We're using a quite famous javascript library called React. It allows us to create reusable components for our user interface. It has a huge gain in performance because of something called 'state'. If your code needs to change just a small part of your UI, the state thingy knows that everything else is still the same and therefore doesn't need to reload everything - just what's new. You can find how-tos at [React Documentation](https://reactjs.org/docs/getting-started.html).

## Back-End ##

The ~~MEAN~~ MEN Stack (as we've replaced Angular with React :relaxed:): MongoDB + Express.js + Node.js. First of all: it's javascript everywhere :thumbsup: But the next logical question is why react over angular? In the end, it's just a matter of personal preference, but that prefence is based on some principles: angular can be too tight with its model/vies and that can be tricky as the app grows; also, react has states :heart: :heart: Having states beats pretty much anything else.

[Node.js](https://nginx.org/en/docs/) comes in not only as a web server, but it also serves as runtime environment for javascript, load balancer for traffic, and allows the use of web sockets to send data to the client instead of just waiting for requests, which makes it the perfect tech to use in real-time apps like ours.

Since we have Node on our side, [Express.js](http://expressjs.com/en/guide/routing.html) comes along with it, being the framework-of-choice to make better use of node. It controls all things related to routes and enables your to control exactly what the client gets depending on its request.

Finally, our data needs to be stored somewhere. Since we're all abut JS, why not a JSON-like database?? :smirk:
[MongoDB](https://docs.mongodb.com/manual/introduction/) is a non-relation database - so put aside for a sec your SQL skills and switch tricky joins for friendy arrays! :wink: Mongo can scale up pretty easily, aside from being very reliable.

## More ##

Other things not mentioned above are the use of [Bootstrap](https://getbootstrap.com/docs/4.1/getting-started/contents/) to make our app responsive, wihch allows our customers to check their stocks anywhere from any device. We also have some DevOps techs to support our delivery: [Nginx](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/?_ga=2.234090782.1697242796.1533827806-1150088802.1533827806) as a much lighter and faster server, [Docker](https://docs.docker.com/get-started/) containers in case we need multiple instances, [Grunt](https://gruntjs.com/getting-started) to automate QA tasks and other repetitive tasks, [Bower](https://bower.io/#getting-started) to manage packages for all these techs we're talking about, and [Jenkins](https://jenkins.io/doc/) as a CI/CD tool to build and deploy our code. These tools combined allow us to be ready to expand the app.

And finally, you can follow up our iterations here [@Trello](https://trello.com/b/IejJoUxi/product-demo-app).