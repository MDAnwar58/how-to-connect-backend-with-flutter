
# How to Connected Backend With Flutter.

At first create flutter product and create backend laravel or any things. Then backend run use that.
```
php artisan serve --host=0.0.0.0 --port=8000
```
or
```
php artisan serve
```

Go to flutter prodect and there go to the file 
```android/app/src/main/AndroidManifest.xml```
and then paste that there. ```android:networkSecurityConfig="@xml/network_security_config"```

```
<application
        android:label="my_app"
        android:name="${applicationName}"
        android:icon="@mipmap/ic_launcher"
        android:networkSecurityConfig="@xml/network_security_config">
</application>
```

And then go to there create that folder and file `xml/network_security_config.xml` and then paste there that.
```
<?xml version="1.0" encoding="utf-8"?>
<network-security-config>
    <domain-config cleartextTrafficPermitted="true">
        <domain includeSubdomains="true">10.0.2.2</domain>
        <domain includeSubdomains="true">localhost</domain>
        <domain includeSubdomains="true">192.168.43.115</domain>
    </domain-config>
</network-security-config>
```

Then workable backend with flutter product

