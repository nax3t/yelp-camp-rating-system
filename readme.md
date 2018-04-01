# Star Rating - Yelp Camp

## Steps (These instructions are incomplete)

- Add [starability CSS](https://github.com/LunarLogic/starability) to public/stylesheets and link to it in views/partials/header.ejs
- Create a public/starability-images directory and add starability's icons.png and icons@2x.png to it
- Replace the form inside of views/campgrounds/show.ejs with:

```
<form action="/campgrounds/<%= campground._id %>/comments" method="POST">
    <div class="form-group">
        <label for="text">Comment:</label>
        <input class="form-control" id="text" type="text" name="comment[text]" placeholder="text">
    </div>
    <label for="rating">Rating:</label>
    <fieldset class="starability-basic form-group" id="rating">
      <input type="radio" id="first-rate5" name="rating[rating]" value="5" />
      <label for="first-rate5" title="Amazing">5 stars</label>
      <input type="radio" id="first-rate4" name="rating[rating]" value="4" />
      <label for="first-rate4" title="Very good">4 stars</label>
      <input type="radio" id="first-rate3" name="rating[rating]" value="3" />
      <label for="first-rate3" title="Average">3 stars</label>
      <input type="radio" id="first-rate2" name="rating[rating]" value="2" />
      <label for="first-rate2" title="Not good">2 stars</label>
      <input type="radio" id="first-rate1" name="rating[rating]" value="1" />
      <label for="first-rate1" title="Terrible">1 star</label>
    </fieldset>
    <div class="form-group">
        <button class="btn btn-lg btn-primary btn-block">Submit!</button>
    </div>
</form>
```

# To do:
- fix flash messages
- allow user to update his/her rating
- finish writing tutorial
- record lecture
