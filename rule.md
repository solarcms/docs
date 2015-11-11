Solar CMS development rules
=========

Package routing rule
----

```php
http://domainname.com/<module_name>/*
```

if route is referenced in admin module

```php
http://domainname.com/solar/<module_name>/*
```

Example package route

```php
Route::group([
    'namespace' => 'Solarcms\UserManager\Http\Controllers',
    'prefix' => 'solar/usermanager',
    'as' => 'Solar.usermanager::'], function () {

    Route::get('user', [
            'as' => 'users',
            'uses' => 'UserController@index']
    );
})
```

