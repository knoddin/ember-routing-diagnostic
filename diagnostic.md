# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The Ember router is where the routes for the application are mapped. For
    example, if you have an 'about' view, you would want to indicate
    the path here (this.route('about') etc.)

    The Ember route is where the model for the data lives. It is the main
    source for the structure of the data.

    source: class notes
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    In the template for boston, nested under campus, you would want to code:
    ```
    {{#link-to 'campus'}}Back{{/link-to}}
    ```

    source: class notes
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first one (beause of the function) indicates that the product route is
    nested under the products route.

    The second one indicates that the product route is its own route to a singular
    product.

    source: class notes
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    In the route.js file of movies model, you would want to reference the data params
    array
    ```
    [params.movie_id];
    ```

    source: class notes
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    {{#link-to}}

    source: class notes
    ```
