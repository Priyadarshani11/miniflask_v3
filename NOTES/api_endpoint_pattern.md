### API endpoints

- GET
  - public (https://xkcd.com/614/info.0.json)
  - private (https://api.twitter.com/1.1/statuses)
  
  - response validation
  

- POST
  - request body validation
  - business logic
  - response validation


### What is service?
Process that is continuously running


### Monolithic application


### micro-service application
We do logical separation of each unit of tasks.


Pros -
  - Your entire web application cannot go down at the same time.
  - Maintainable software


### Validator

- validators are "class methods", so the first argument value they receive is the UserModel class, not an instance of UserModel.
  the second argument is always the field value to validate; it can be named as you please
- you can also add any subset of the following arguments to the signature (the names must match):
    - values: a dict containing the name-to-value mapping of any previously-validated fields
    - config: the model config
    - field: the field being validated. Type of object is pydantic.fields.ModelField.
    - **kwargs: if provided, this will include the arguments above not explicitly listed in the signature
- validators should either return the parsed value or raise a ValueError, TypeError, or AssertionError (assert statements may be used).