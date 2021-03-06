# Base Path Middleware for PHP

This middleware just removes a prefix from the request uri. 

## Usage

Just add the middleware as one of the first in your application.

For example:
```php
$app->pipe(new \LosMiddleware\BasePath\BasePath('/site');
```

Every request with `/site` prefix will be replaced:
```
/site => /
/site/blog => /blog
/site/contact-us => /contact-us
```

### Zend Expressive

If you are using [expressive-skeleton](https://github.com/zendframework/zend-expressive-skeleton), you can copy `config/los-basepath.global.php.dist` to `config/autoload/los-basepath.global.php` and modify configuration as your needs.
