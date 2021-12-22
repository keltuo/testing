## Composer packages for dev
```
"require-dev": {
    "phpstan/phpstan": "^1.2.0",
    "phpunit/phpunit": "^9",
    "slevomat/coding-standard": "^7.0",
    "squizlabs/php_codesniffer": "*",
    "micheh/phpcs-gitlab": "*"
}
```

## Symfony packages for testing
```
"require-dev": {
    ...
    "symfony/phpunit-bridge": "5.4.*",
    "symfony/browser-kit": "5.4.*",
    "symfony/css-selector": "5.4.*",
    "symfony/maker-bundle": "^1.29",
    "jetbrains/phpstorm-attributes": "^1.0",
}
```


## Support PHP Storm docker testing
Configuration files
```
  .run / 
```

1. step - create images
```
  docker-compose -f docker-compose-unit.yml up
```

2. step - create docker interpreter in PHP Storm configuration
   1. Add Configuration - Command line box click at "..." after "Choose interpreter dropdown"
      ![Add Configuration](img/phpstorm/step%201.png)
   2. Click '+' (new cli interpreter) - choose from docker
      ![Add cli interpreter](img/phpstorm/step%202.png)
   3. Configure remote interpreter - Choose "Docker compose"
      ![Configure cli interpreter](img/phpstorm/step%203.png)
   4. Configure remote interpreter - Choose from dropdown "Configuration files" and new Click at '+' and choose your "docker-compose-unit.yml"
      ![Configure cli interpreter](img/phpstorm/step%204.png)
   5. Choose service "php" (service in docker-compose file)
      ![Configure cli interpreter](img/phpstorm/step%205.png)
   6. Click 'ok' and then 'apply'
      ![Configure cli interpreter](img/phpstorm/step%206.png)
   7. Choose you new remote interpreter from dropdown
      ![Configure cli interpreter](img/phpstorm/step%207.png)
   8. Run script list in PHP storm -> choose one and run on green arrow ">" :)
      ![Configure cli interpreter](img/phpstorm/step%208.png)

thx

