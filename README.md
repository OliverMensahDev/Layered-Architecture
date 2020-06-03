# Layered-Architecture
![alt text](https://raw.githubusercontent.com/OliverMensahDev/content-resources/master/uml/monolithic.png)

The diagram above is a typical monolith application that fetches data from a data source and renders that to a certain user 
interface, in this case, a web browser. 
First, the application is structured to contain `View` -- the actual user interface elements, in this case, a list of items 
displayed in the browser.
It also has a `Presentation` layer that contains logic for driving our UI. 
Here, anytime the web browser loads, a method call is made to retrieve all people and populate the browser with such data. 
Then we have our `Repository layer`, here it is called PersonRepository and this is a repository that's responsible for 
interacting with Service which could be a data store.
And the bottom layer is the `Service` layer, helps to provide data for the application, it can database, API or any data store. 
Currently,the application service uses a hardcoded array of data.
