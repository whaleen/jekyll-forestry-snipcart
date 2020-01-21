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