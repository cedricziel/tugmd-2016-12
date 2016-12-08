---

# Composer, Transladder, Docker

## Ein Rundumschlag

---

# Composer {.big}

> Dependency management für PHP
> > getcomposer.org

---

# Composer (Demo 1/2)

* [Composer](https://getcomposer.org/)
* [Packagist](https://packagist.org)
  * [FluidTYPO3 auf Packagist](https://packagist.org/search/?q=fluidtypo3)
  * [Symfony auf Packagist](https://packagist.org/search/?q=symfony)
  * [TYPO3 Distribution auf GitHub](https://github.com/cedricziel/typo3-base-distribution)

---

# Composer (Demo 2/2)

```bash
# initialisieren
composer create-project \
  cedricziel/typo3-base-distribution \ # Quelle
  mein-tolles-projekt \                # Name des Projektes / Verzeichnis
  dev-master                           # Version der Vorlage

# Copy & Paste me
composer create-project cedricziel/typo3-base-distribution mein-tolles-projekt dev-master
```

---

# Docker {.big}

Leichtgewichtige Prozesscontainer

---

# Und alle zusammen..

```bash
# Starte container aus yml definition
docker-compose up (-d)

# Liste laufende container
docker-compose ps

# Aktualisiere Container
docker-compose pull
```

---

# TYPO3 über die Kommandozeile initialisieren

```bash
vendor/bin/typo3cms install:setup \
    --non-interactive \
    --database-user-name=typo3 \
    --database-user-password=typo3 \
    --database-host-name=127.0.0.1 \
    --database-port=33060 \
    --database-name=typo3 \
    --use-existing-database \
    --admin-user-name=admin \
    --admin-password=password \
    --site-setup-type=site
```

---

# TYPO3 - Login

```bash
php -S 127.0.0.1:8000 -t web/
```

> Login: admin / password

---

# TYPO3 - Extensions installieren

```javascript
{
  "repositories": [
    {
      "type":"vcs",
      "url":"https://github.com/cedricziel/mask.git"
    }
  ]
}
```

```bash
composer require "mask/mask dev-fixme"
```

---

# Transladder

> do weird things to your content
> [github.com/cedricziel/transladder](https://github.com/cedricziel/transladder)

---

# Transladder (Installation)

```bash
composer require cedricziel/transladder
```

---

# Transladder Demo {.big}
