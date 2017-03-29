# [historias.datos.gob.ar](http://historias.datos.gob.ar/)
Página de inicio para visualizaciones del [Portal de Datos](http://datos.gob.ar/) de la República Argentina.

## Índice 
* [Instalación](#instalación) 
* [Contacto](#contacto) 

## Instalación 
* Instalar Apache: `sudo apt install apache2`
* Clonar el repositorio en `/var/www`
* Modificar permisos:

    `sudo chown -R $USER:$USER /var/www/historias.datos.gob.ar`

    `sudo chmod -R 755 /var/www`

### Configuración de Apache
* Crear y editar el archivo de configuración para el sitio:

    `sudo vi /etc/apache2/sites-available/historias.datos.gob.ar.com.conf`

    Ejemplo:
    ```
    Listen 80
    <VirtualHost *:80>
            ServerName historias.datos.gob.ar.com

            ServerAdmin webmaster@localhost
            DocumentRoot /var/www/historias.datos.gob.ar/

            ErrorLog ${APACHE_LOG_DIR}/error.log
            CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>
    ```
* Habilitar el sitio: `sudo a2ensite historias.datos.gob.ar.com`
* Reiniciar el servidor: `sudo service apache2 restart`

## Contacto
Te invitamos a [crearnos un issue](https://github.com/datosgobar/historias.datos.gob.ar/issues/new?title=Encontre-un-bug-en-historias.datos.gob.ar) en caso de que encuentres algún bug o tengas comentarios de alguna parte de `historias.datos.gob.ar`. Para todo lo demás, podés mandarnos tu sugerencia o consulta a [datos@modernizacion.gob.ar](mailto:datos@modernizacion.gob.ar).
