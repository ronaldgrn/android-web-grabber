# android-web-grabber
A small class to quickly get web requests on android

Note
----

This was quickly spun up for a small, short-lived project. I cannot guarantee that it will always work as expected or that it is a recommended way of doing HttpRequests.


How to use
----------

1. Create a new instance of WebGrabber class, overriding getResponse.

2. Set the request url with either 
`.setUrlFromString("https://jsonplaceholder.typicode.com/posts");`
or 
`.setUrl(URL Object);`

3. run `.fetch`.

The overridden getResponse will be called with the resulting string.


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
