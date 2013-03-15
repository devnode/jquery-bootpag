bootpag - dynamic pagination jQuery plugin
==========================================

This jQuery plugin helps you create dynamic pagination with [twitter bootstrap](http://twitter.github.com/bootstrap) or in any other html pages.

#Example

Snippet that dynamic loads number of pages.
More examples can be found on [project homepage](http://botmonster.github.com/jquery-bootpag)

```html
<p id="content">Dynamic page content</p>
<p id="pagination-here"></p>
```

```javascript
$('#pagination-here').bootpag({
    total: 38,          // total pages
    page: 1,            // default page
    maxVisible: 9,     // visible pagination, must be odd. if even, maxVisible--.
    leaps: true         // next/prev leaps through maxVisible
}).on("page", function(event, num){
    $("#content").html("Page " + num); // or some ajax content loading...
}); 

```
#License

Plugin available under MIT license (see LICENSE.txt)

#Reason for the fork?!

maxVisible value was not consistent with the current page. This fork will always display a minimum of the maxVisible value.

Example:
```
< [1] 2 3 4 5 6 7 8 9 >
< 7 8 9 10 11 12 13 14 [15] >
```
