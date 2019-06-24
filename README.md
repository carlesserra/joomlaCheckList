# Joomla Check List
Coses a tenir en compte en un Joomla per entregar al client final

## Configuració
En l'apartat de configuració és important tenir en compte el següent:

* Email del sistema canviar per el del client
* Paths de logs i tmp modificar pels del servidor final d'allotjament
* Urls amigables i activar mod_rewrite amb htaccess
* Error reporting "None"
* Activar la compressió de pàgines amb Gzip
* Gestió de sessions amb PHP en comptes de la base de dades

## Integració amb Google

* Google Recaptcha
* Google Maps (es necessita tarja crèdit client)
* Google Analytics
* Google Search Console (antigament Google Webmaster Tools)
* Google My Business (sitemap)

## Extensions
Algunes extensions necessàries en qualsevol instal·lació:

* Email as username (properament inclós en el JPFramework)
* Secure Login
* Mòdul administració Afi Notify per mostrar publicitat
* Component per crear sitemap
* Component Akeeba Backup (estic valorant opció d'instal·lar Akeeba Backup Pro)

## SSL
Si tenim el com_botiga i fem servir redsys a la configuració global ha de desactivar-se el ssl i al htaccess afegir aquestes linies al final:

~~~
##configuració especifica per redsys sota ssl
RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteCond %{QUERY_STRING} !(^|&)view=callback(&|$)
RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
~~~

## Configuració SEO

* Tinc recopilades una sèrie de recomanacions SEO. Crec que seria interessant parlar-ne un dia per definir el "SEO bàsic" que oferim en els packs
