#Se trata de una sencilla aplicación realizada con PhoneGap-Cordova.

#Pasos a seguir para iniciar el proyecto y poner a funcionar el servidor:

1-Desde un terminal (en mi caso el node.js command prompt):

phonegap

2-Nos situamos en el directorio Phonegap (en la que queremos crear el proyecto).

phonegap create MyApp

MyApp es el nombre del proyecto.

cd MyApp

3-Ahora estamos en el directorio del proyecto
Tenemos una serie de subdirectorios:
En www tenemos el proyecto en si, con su css y su index.html (que visualizaremos en el navegador web).

phonegap serve

4-Hemos arrancado el servidor con node.js para nuestra app, tenemos la dirección ip y puerto para acceder en el
navegador web.

Si hacemos algún cambio en nuestro index.html este se hace en tiempo real.
En el subdirectorio platforms tenemos las herramientas para exportar nuestra app.

phonegap platform

Nos muestra las plataformas

phonegap run android

Nos instala automáticamente la plataforma para android (generaría un archivo .apk)

#Implementaciones realizadas:
-Utilización de cámara con el método camera.getPicture() y dando una uri para la imagen.
-Utilización de Vibración con el método navigator.vibrate().
-Utilización de estado de la batería con el método onBatteryStatus().
-Proximamente: Brújula con compass.getCurrentHeading() y compass.watchHeading()

#Documentacion y enlaces consultados:
-Cámara:
https://cordova.apache.org/docs/es/3.1.0/cordova/camera/camera.html
https://www.adictosaltrabajo.com/tutoriales/acceso-camara-phonegap/
-Brújula(en proceso):
https://cordova.apache.org/docs/es/3.1.0/cordova/compass/compass.html
-Vibración:
https://cordova.apache.org/docs/en/latest/reference/cordova-plugin-vibration/

# Hello World PhoneGap Template [![bitHound Score][bithound-img]][bithound-url]

A PhoneGap Hello World template

## Usage

#### PhoneGap CLI

The hello-world template is the default when you create a new application using the [phonegap-cli][phonegap-cli-url].

    phonegap create my-app

Create an app using this template specifically:

    phonegap create my-app --template hello-world

To see a list of other available PhoneGap templates:

    phonegap template list

## [config.xml][config-xml]

#### android-minSdkVersion (Android only)

Minimum SDK version supported on the target device. Maximum version is blank by default.

This template sets the minimum to `14`.

    <preference name="android-minSdkVersion" value="14" />

#### &lt;access ...&gt; (All)

This template defaults to wide open access.

    <access origin="*" />

It is strongly encouraged that you restrict access to external resources in your application before releasing to production.

For more information on whitelist configuration, see the [Cordova Whitelist Guide][cordova-whitelist-guide] and the [Cordova Whitelist Plugin documentation][cordova-plugin-whitelist]

## [www/index.html][index-html]

#### Content Security Policy (CSP)

The default CSP is similarly open:

    <meta http-equiv="Content-Security-Policy" content="default-src * 'unsafe-inline'; style-src 'self' 'unsafe-inline'; media-src *" />

Much like the access tag above, you are strongly encouraged to use a more restrictive CSP in production.

A good starting point declaration might be:

    <meta http-equiv="Content-Security-Policy" content="default-src 'self' data: gap: 'unsafe-inline' https://ssl.gstatic.com; style-src 'self' 'unsafe-inline'; media-src *" />

For more information on the Content Security Policy, see the [section on CSP in the Cordova Whitelist Plugin documentation][cordova-plugin-whitelist-csp].

Another good resource for generating a good CSP declaration is [CSP is Awesome][csp-is-awesome]


[phonegap-cli-url]: http://github.com/phonegap/phonegap-cli
[cordova-app]: http://github.com/apache/cordova-app-hello-world
[bithound-img]: https://www.bithound.io/github/phonegap/phonegap-app-hello-world/badges/score.svg
[bithound-url]: https://www.bithound.io/github/phonegap/phonegap-app-hello-world
[config-xml]: https://github.com/phonegap/phonegap-template-hello-world/blob/master/config.xml
[index-html]: https://github.com/phonegap/phonegap-template-hello-world/blob/master/www/index.html
[cordova-whitelist-guide]: https://cordova.apache.org/docs/en/dev/guide/appdev/whitelist/index.html
[cordova-plugin-whitelist]: http://cordova.apache.org/docs/en/latest/reference/cordova-plugin-whitelist
[cordova-plugin-whitelist-csp]: http://cordova.apache.org/docs/en/latest/reference/cordova-plugin-whitelist#content-security-policy
[csp-is-awesome]: http://cspisawesome.com
