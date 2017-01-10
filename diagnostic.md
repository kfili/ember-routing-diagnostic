# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    - The Ember Router tells the parses the requests from the client and calls
    functions that will display react and render things according to the
     request.
     - a route will determine where and how data is send down and actions are
       sent up.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    The question states the route we have, and that we need a 'link-to', but not
    what we are linking to or what an appropriate link is, or where we are
    linking from. What am i missing?
    {{#link-to 'campus.boston'}}Link to Boston Campus{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀 here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    - the first definition is does not nest individual products under the
    products route.
    - the first block of code nests 'this.route' in a callback for
    another 'this.route'.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```js
    model (params) {
      return this.get('store').findRecord('movies', params.movie_id);
    },
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    By using a model and a component similar to the example used in yesterdays
    code along, such as listr-list.
    ```
