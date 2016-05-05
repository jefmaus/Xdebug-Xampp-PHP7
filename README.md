Habilitar Xdebug en XAMPP con PHP7

Para habilitar Xdebug en XAMPP con la nueva versión de PHP7, debemos hacer los siguientes pasos:

1. Descargar el archivo php_xdebug.dll y pegarlo en la carpeta "ext" dentro de la carpeta "php" en la ruta donnde se instalo xampp.

C:\xampp\php\ext

2. Abrir el archivo php.ini y agregar las siguientes lineas:

[XDebug]
zend_extension = "c:\xampp\php\ext\php_xdebug.dll"
xdebug.profiler_append = 0
xdebug.profiler_enable = 0
xdebug.profiler_enable_trigger = 0
xdebug.profiler_output_dir = "c:\xampp\tmp"
;xdebug.profiler_output_name = "cachegrind.out.%t-%s"
xdebug.remote_enable = 1
xdebug.remote_handler = "dbgp"
xdebug.remote_host = "127.0.0.1"
xdebug.remote_log="c:\xampp\tmp\xdebug.txt"
xdebug.remote_port = 9000
xdebug.trace_output_dir = "c:\xampp\tmp"
; 3600 (1 hour), 36000 = 10h
xdebug.remote_cookie_expire_time = 36000

3. Finalmente solo hay que reiniciar el servidor Apache y listo, ya puede utilizar xdebug.
