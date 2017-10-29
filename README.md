<p align="center">
  <img src="https://s3.amazonaws.com/ohmyzsh/oh-my-zsh-logo.png" alt="Oh My Zsh">
</p>

Oh My Zsh es un framework de código abierto, impulsado por la comunidad, para gestionar su configuración [zsh](http://www.zsh.org/).

Suena aburrido. Intentémoslo de nuevo.

__Oh My Zsh no te convertirá en un desarrollador de 10x... pero tal vez te sientas como uno.__

Una vez instalado, su terminal shell se convertirá en el tema de la ciudad o le devolvemos su dinero! Con cada pulsación de teclado en la línea de comandos, se beneficiará de los cientos de potentes plugins y hermosos temas. Extraños se acercarán a ti en los cafés y te preguntarán: _"¡Eso es increíble! ¿Eres algún tipo de genio?"_

Finalmente, usted comenzará a recibir el tipo de atención que siempre ha sentido que se merecía. ... o tal vez use el tiempo que ahorra para empezar a usar el hilo dental con más frecuencia.

Para saber más, visita [ohmyz.sh](http://ohmyz.sh) y sigue [@ohmyzsh](https://twitter.com/ohmyzsh) en Twitter.

## Primeros pasos

### Prerrequisitos

__Descargo de responsabilidad:__ _Oh My Zsh funciona mejor en macOS y Linux._

* Sistema operativo tipo Unix (macOS o Linux)
* [Zsh](http://www.zsh.org) debe ser instalado (v4.3.9 o más reciente). Si no está preinstalado  (`zsh --version` para confirmar), , compruebe la siguiente instrucción aquí: [Instalación de ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
* `curl` o `wget` debe estar instalado
* `git` debe instalarse

### Instalación básica

Oh My Zsh se instala ejecutando uno de los siguientes comandos en su terminal. Puede instalarlo a través de la línea de comandos con `curl` o `wget`.

#### via curl

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### via wget

```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

## Usando Oh My Zsh

### Plugins

Oh My Zsh viene con un montón de plugins para aprovechar. Puedes echar un vistazo en el directorio de [plugins](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins) y/o la [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) para ver lo que está disponible actualmente.

#### Habilitación de Plugins

Una vez que localices un plugin (o varios) que te gustaría usar con Oh My Zsh, necesitarás habilitarlos en el archivo `.zshrc`. YEncontrarás el archivo zshrc en tu directorio `$HOME`. OÁbrelo con tu editor de texto favorito y verás un lugar para listar todos los plugins que quieras cargar.

Por ejemplo, esta línea podría empezar a verse así:

```shell
plugins=(git bundler osx rake ruby)
```

#### Uso de Plugins

La mayoría de los plugins (¡deberían! estamos trabajando en esto) incluyen un __README__, que documenta cómo usarlos.

### Temas

Lo admitiremos. Temprano, en el mundo de Oh My Zsh, puede que nos hayamos puesto demasiado optimistas con los temas. Tenemos más de cien temas incluidos. La mayoría de ellos tienen [capturas de pantalla](https://wiki.github.com/robbyrussell/oh-my-zsh/themes) en la wiki. Echa un vistazo!

#### Selección de un Tema

_El tema de Robby es el tema por defecto. No es el más elegante. No es el más simple. Es el correcto (para él)._

OUna vez que encuentre el tema que desea usar, necesitará editar el archivo `~/.zshrc`. Verás una variable de entorno (todo en mayúsculas) ahí que parece algo como esto:

```shell
ZSH_THEME="robbyrussell"
```

Para utilizar un tema diferente, simplemente cambie el valor para que coincida con el nombre del tema deseado. Por ejemplo:

```shell
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# you might need to install a special Powerline font on your console's host for this to work
# see https://github.com/robbyrussell/oh-my-zsh/wiki/Themes#agnoster
```

Abra una nueva ventana de terminal y su terminal debería ser algo parecido a esto:

![Agnoster theme](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

En caso de que no hayas encontrado un tema adecuado para tus necesidades, por favor echa un vistazo a la wiki para ver [más de ellos](https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes).

Si te sientes con ganas, puedes dejar que el ordenador seleccione uno al azar cada vez que abras una nueva ventana de terminal.


```shell
ZSH_THEME="random" # (...please let it be pie... please be some pie..)
```


## Tópicos Avanzados

Si eres del tipo que le gusta ensuciarse las manos, estas secciones pueden resonar.

### Instalación Avanzada

Es posible que algunos usuarios deseen cambiar la ruta predeterminada o instalar manualmente Oh My Zsh.

#### Directorio Personalizado

La ubicación predeterminada es `~/.oh-my-zsh` (oculta en el directorio home)

Si desea cambiar el directorio de instalación con la variable de entorno `ZSH`, ya sea ejecutando `export ZSH=/your/path` antes de la instalación, o bien configurándolo de esta forma antes de que finalice la instalación:

```shell
export ZSH="$HOME/.dotfiles/oh-my-zsh"; sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### Instalación Manual

##### 1. Clonar el repositorio:

```shell
git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
```

##### 2. *Opcionalmente*, haga una copia de seguridad de su archivo `~/.zshrc` existente:

```shell
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Cree un nuevo archivo de configuración zsh:

You can create a new zsh config file by copying the template that we have included for you.

```shell
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Cambiar el shell predeterminado:

```shell
chsh -s /bin/zsh
```

##### 5. Inicialice su nueva configuración zsh:

Una vez que abra una nueva ventana de terminal, debería cargar zsh con la configuración de Oh My Zsh.

### Problemas de Instalación

Si usted tiene algún error instalando, aquí hay algunas correcciones comunes.

* YEs posible que necesite modificar su `PATH` en `~/.zshrc` si no puede encontrar algunos comandos después de cambiar a `oh-my-zsh`.
* Si ha instalado manualmente o cambiado la ubicación de instalación, compruebe la variable de entorno `ZSH` en `~/.zshrc`.

### Plugins y Temas Personalizados

Si desea anular cualquiera de los comportamientos predeterminados, sólo tiene que añadir un nuevo archivo (que termine en `.zsh`) n el directorio `custom/`.

Si tienes muchas funciones que van bien juntas, puedes ponerlas como un archivo `XYZ.plugin.zsh` en el directorio `custom/plugins/` y luego habilitar este plugin.

Si desea anular la funcionalidad de un plugin distribuido con Oh My Zsh, cree un plugin del mismo nombre en el directorio `custom/plugins/` y se cargará en lugar del que se encuentra en `plugins/`.

## Obtener Actualizaciones

De forma predeterminada, se le pedirá que compruebe las actualizaciones cada pocas semanas. Si desea que `oh-my-zsh` tse actualice automáticamente sin necesidad de que se le pregunte, configure lo siguiente en su `~/.zshrc`:

```shell
DISABLE_UPDATE_PROMPT=true
```

TPara desactivar las actualizaciones automáticas, configure lo siguiente en su `~/.zshrc`:

```shell
DISABLE_AUTO_UPDATE=true
```

### Actualizaciones Manuales

Si desea actualizar en cualquier momento (quizás alguien acaba de lanzar un nuevo plugin y no quiere esperar una semana?), sólo necesita ejecutar:

```shell
upgrade_oh_my_zsh
```

¡Magia!

## Desinstalación de Oh My Zsh

Oh My Zsh no es para todos. Te echaremos de menos, pero queremos que esto sea una ruptura fácil.

Si desea desinstalar `oh-my-zsh`, simplemente ejecute `uninstall_oh_my_zsh` desde la línea de comandos. Se eliminará y revertirá tu anterior configuración `bash` o `zsh`.

## Contribuir

Estoy lejos de ser un experto en [Zsh](http://www.zsh.org/) y sospecho que hay muchas maneras de mejorar - si tienes ideas sobre cómo hacer que la configuración sea más fácil de mantener (y más rápida), no dudes en hacer un fork y enviar solicitudes de pull!

También necesitamos gente que pruebe las solicitudes de pull. Así que echa un vistazo a los problemas pendientes](https://github.com/robbyrussell/oh-my-zsh/issues) y ayúdanos donde puedas.

### NO nos envíe temas

Tenemos (más que) suficientes temas por el momento. Por favor, añade tu tema a la página wiki de [temas externos](https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes).

## Colaboradores

Oh My Zsh tiene una comunidad vibrante de usuarios felices y colaboradores encantadores. Sin todo el tiempo y la ayuda de nuestros colaboradores, no sería tan impresionante.

¡Muchísimas gracias!

## Síguenos

Estamos en las redes sociales.

* [@ohmyzsh](https://twitter.com/ohmyzsh)  en Twitter. Deberías seguirlo.
* [Oh My Zsh](https://www.facebook.com/Oh-My-Zsh-296616263819290/) en Facebook.

## Mercancía

Tenemos [stickers](http://shop.planetargon.com/products/ohmyzsh-stickers-set-of-3-stickers) y [camisetas](http://shop.planetargon.com/products/ohmyzsh-t-shirts)  para que puedas mostrar tu amor por Oh My Zsh. Una vez más, esto le ayudará a convertirse en el tema de conversación de la ciudad!

## Licencia

Oh My Zsh es liberado bajo la [licencia del MIT](LICENSE.txt).

## Acerca de Planet Argon

![Planet Argon](http://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh fue fundado por el equipo de [Planet Argon](https://www.planetargon.com/?utm_source=github), una [agencia de desarrollo de Ruby on Rails](https://www.planetargon.com/skills/ruby-on-rails-development?utm_source=github).
