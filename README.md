# Frontend Mentor - Product preview card component

[Link to the challenge](https://www.frontendmentor.io/solutions/product-preview-card-component-rjWA0WL-IT)

[Live preview](https://jionnymagiah.github.io/product-preview-card-component-main/)
## Aim of the project:
Replicate the following result summary component 

![](./design/desktop-design.jpg)

## Styles
The colors, font and font size were provided by Frontend Mentor. Margins and paddings were not provided, and I've fixed them by fine-tuning.

## Data
Name, price and description of the project are hard-coded inside the html page.

## Technology used
Due to the absence of any data or dynamics, the solution is a static page built with html and css.

In a real scenario I would build a custom component for the card. In particular, using Svelte I would define a component like `Product.svelte`
```html
<script>
    export let name;
    export let desc;
    export let priceFull;
    export let priceSales;
    export let category;
</script>

<div class="right">
    <div class="category">
        {category}
    </div>
    <div class="product-name">
        {name}
    </div>
    <div class="product-desc">
        {desc}
    </div>
    <div class="price">
        <div class="sale-price">
            {priceSales}
        </div>
        <div class="full-price">
            {priceFull}
            </div>
    </div>
    <button>
        <div>
            <img src="images/icon-cart.svg" alt="" srcset="">
            <span>
                Add to Cart
                </span>
        </div>
    </button>
</div>

<style>
<!--- CSS style for the component--->
</style>
```
and use it as
```html
<Product {...productData} />
```




## Todo
The responsive layout will be implemented soon.