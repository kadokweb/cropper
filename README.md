# Cropper @KadokWeb

[![Maintainer](http://img.shields.io/badge/maintainer-@kadokweb-blue.svg?style=flat-square)](https://twitter.com/kadokweb)
[![Source Code](http://img.shields.io/badge/source-kadokweb/cropper-blue.svg?style=flat-square)](https://github.com/kadokweb/cropper)
[![PHP from Packagist](https://img.shields.io/packagist/php-v/kadokweb/cropper.svg?style=flat-square)](https://packagist.org/packages/kadokweb/cropper)
[![Latest Version](https://img.shields.io/github/release/kadokweb/cropper.svg?style=flat-square)](https://github.com/kadokweb/cropper/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build](https://img.shields.io/scrutinizer/build/g/kadokweb/cropper.svg?style=flat-square)](https://scrutinizer-ci.com/g/kadokweb/cropper)
[![Quality Score](https://img.shields.io/scrutinizer/g/kadokweb/cropper.svg?style=flat-square)](https://scrutinizer-ci.com/g/kadokweb/cropper)
[![Total Downloads](https://img.shields.io/packagist/dt/kadokweb/cropper.svg?style=flat-square)](https://packagist.org/packages/kadokweb/cropper)

###### Cropper is a component that simplifies the creation of JPG and PNG image thumbnails with a cache engine. Cropper CC creates your image for each part required in the application with zero complexity.

Cropper é um componente que simplifica a criação de miniaturas de imagens JPG e PNG com um motor de cache. O Cropper CC cria versões de suas imagens para cada dimensão necessária na aplicação com zero de complexidade.

####WEBP THUMBNAILS:

Published in version 1.3.\* by default how thumbnails are converted to webP.

Adicionado na versão 1.3.\* por padrão as miniaturas são convertidas para webP.

## About KadokWeb

###### KadokWeb is a set of small and optimized PHP components for common tasks. Held by Doka Silva and the UpInside team. With them you perform routine tasks with fewer lines, writing less and doing much more.

KadokWeb é um conjunto de pequenos e otimizados componentes PHP para tarefas comuns. Mantido por Doka Silva e a equipe UpInside. Com eles você executa tarefas rotineiras com poucas linhas, escrevendo menos e fazendo muito mais.

### Highlights

- Simple Thumbnail Creator (Simples criador de miniaturas)
- Cache optimization per dimension (Otimização em cache por dimensão)
- Media Control by Filename (Contrôle de mídias por nome do arquivo)
- Cache cleanup by filename and total (Limpeza de cache por nome de arquivo e total)
- Composer ready and PSR-2 compliant (Pronto para o composer e compatível com PSR-2)

## Installation

Cropper is available via Composer:

```bash
"kadokweb/cropper": "1.3.*"
```

or run

```bash
composer require kadokweb/cropper
```

## Documentation

###### They are just two methods to do all the work. You just need to call **_make_** to create or use thumbnails of any size, or **_flush_** to free the cache of a file or the entire folder. KadokWeb Cropper works like this:

São apenas dois métodos para fazer todo o trabalho. Você só precisa chamar o **_make_** para criar ou usar miniaturas de qualquer tamanho, ou o **_flush_** para liberar o cache de um arquivo ou da pasta toda. KadokWeb Cropper funciona assim:

#### Create thumbnails

```php
<?php
require __DIR__ . "/../src/Cropper.php";

$c = new \KadokWeb\Cropper\Cropper("patch/to/cache");

echo "<img src='{$c->make("images/image.jpg", 500)}' alt='Happy Coffee' title='Happy Coffee'>";
echo "<img src='{$c->make("images/image.jpg", 500, 300)}' alt='Happy Coffee' title='Happy Coffee'>";
```

#### Clear cache

```php
<?php
require __DIR__ . "/../src/Cropper.php";

$c = new \KadokWeb\Cropper\Cropper("patch/to/cache");

//flush by filename
$c->flush("images/image.jpg");

//flush cache folder
$c->flush();
```

## Contributing

Please see [CONTRIBUTING](https://github.com/kadokweb/cropper/blob/master/CONTRIBUTING.md) for details.

## Support

###### Security: If you discover any security related issues, please email doka@kadok.com.br instead of using the issue tracker.

Se você descobrir algum problema relacionado à segurança, envie um e-mail para doka@kadok.com.br em vez de usar o rastreador de problemas.

Thank you

## Credits

- [Doka Silva](https://github.com/kadokweb) (Developer)
- [KadokWeb](https://github.com/kadokweb) (Team)
- [All Contributors](https://github.com/kadokweb/cropper/contributors) (This Rock)

## License

The MIT License (MIT). Please see [License File](https://github.com/kadokweb/cropper/blob/master/LICENSE) for more information.
