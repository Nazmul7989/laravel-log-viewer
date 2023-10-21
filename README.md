# Log Viewer Setup Guideline

### Installing the package via Composer
``` 
composer require opcodesio/log-viewer
```

### And publish the front-end assets by running:
``` 
php artisan log-viewer:publish
```

### Publishing the configuration
``` 
php artisan vendor:publish --tag="log-viewer-config"
```

### You can configuration .env file (optional)
``` 
LOG_VIEWER_ENABLED=true
```

### If you want to restrict log viewer for only authenticated user, you need to add this Authenticate middleware in config/log-viewer.php file
``` 

    'middleware' => [
        'web',
        \App\Http\Middleware\Authenticate::class,
    ],
```

### Finally You can view log by (/log-viewer)
``` 
http://your_domain/log-viewer
```
