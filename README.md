# Node.js (Express.js) file structure

*A simple Node.js file structure - my personal preference*

## File structure

```javascript
  APP_ROOT/
    src/
      components/  // A component can access other component through its controller only (not through model)
        users/
          controller.js
          model.js
          routes.js
      associations.js  // All associations/realtions between models
      middlewares.js  // All middlewares like for sending reponse, encrypting password, etc.(must not access any component)
      validators.js  // Clean and validate all incoming data
      util.js  // Utility functions
    config/
      constants.js
      db.js  // Connections to database
      errors.js  // Error formatting functions
    migrations/
      model.field.js  // Migrations in case of a SQL database
    views/
      templates/
        email.html  // Template for sending mail, etc.
      password-reset.html  // Views which are to be rendered from the server
```


## License

(The MIT License)

Copyright (c) 2015 Sachin Bansal

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
