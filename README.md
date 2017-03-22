# android-web-grabber
A small class to quickly get web requests on android

Note
----

This was quickly spun up for a small, short-lived project. I cannot guarantee that it will always work as expected or that it is a recommended way of doing HttpRequests.


How to use
----------

Create a new instance of WebGrabber class, overriding getResponse.
Set the request url with either 
`wg.setUrlFromString("https://jsonplaceholder.typicode.com/posts");`
or 
`wg.setUrl(URL Object);`

run `fetch`.

The overridden getResponse will be called with the string response.


Example
-------

```java
WebGrabber wg = new WebGrabber(){
    @Override
    public void getResponse(String answer){
        Log.d("ANSWER", answer);
    }
};
wg.setUrlFromString("https://jsonplaceholder.typicode.com/posts");
wg.fetch();
```
