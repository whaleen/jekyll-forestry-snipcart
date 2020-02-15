
Don't use this... yet.



### Developing in the Browser

Serve and re-build on the fly
``` bundle exec jekyll serve
```

reload browser when rebuild occurs
``` browser-sync start --files "css/*.css" --proxy "localhost:4000" --files "_site/*" --reloadDelay "1000"
```

### Creating a new Collection

In this case we make the Products collection.
Add to /_config.yml

```
collections:
  products:
    output: true
    permalink: "/products/:path/"
```    


#### Forestry.io setup
Add Products section to /.forestry/settings.yml

```
sections:
- type: directory
  path: _products
  label: Products
  create: all
  match: "*"
  templates:
  - product
```
Note above that templates calls for 'products'. This needs to be created and will reside in /.forestry/front_matter/templates/products.yml

I suggest you build this frontmatter template using the forestry gui.


You will need to create a new layout for the collection and provide this as a hidden field with the default value using it's name.

In this case:

/_layouts/products.html


placeholder images:
https://www.pexels.com/search/exhibition/

placeholder copy:
https://www.descriptionari.com/quotes/the-girl-with-no-name/?h=fashion
