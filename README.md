# metal-autocomplete

Metal's autocomplete component

## Setup

1. Install NodeJS >= [v0.12.0](http://nodejs.org/dist/v0.12.0/), if you don't have it yet.

2. Install global dependencies:

  ```
  [sudo] npm install -g gulp
  ```

3. Install local dependencies:

  ```
  npm install
  ```

4. Build the code:

  ```
  gulp build
  ```

5. Open the demo at demos/index.html on your browser.

<br/>

## How to use

1. Load the component from your path.

  ```
  <script src="autocomplete.js"></script>
  ```

2. Create a new instance.

  ```
  new Autocomplete({
    inputElement: document.querySelector('input'),
    data: function(query) {
      return ['Alabama', 'Alaska'].filter(function(item) {
        return query && item.toLowerCase().indexOf(query.toLowerCase()) === 0;
      });
    }
  });
  ```

3. Options:

- inputElement: The input:text where the user will type the word.

- data: The method to fetch and deal with the data.
