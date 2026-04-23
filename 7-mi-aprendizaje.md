# COMPLETAR  
Antes de esta práctica sabía cómo descargar imágenes desde Docker Hub y crear contenedores a partir de ellas, pero nunca había creado una imagen propia.
Nuevos aprendizajes
El principal aprendizaje fue construir mis propias imágenes usando un Dockerfile, entendiendo que cada instrucción como FROM, RUN, COPY, EXPOSE y CMD genera una capa independiente. También aprendí cómo funciona el caché de Docker, que permite reutilizar capas que no cambiaron y acelerar construcciones posteriores, algo que pude comprobar cuando la versión 2.0 tardó solo 1.6 segundos frente a los 162 de la primera vez. Además conocí qué son las imágenes huérfanas, cómo mapear puertos automáticamente con -P y las distintas políticas de reinicio de contenedores.
Problema resuelto
Al construir la imagen con CentOS 7 los repositorios fallaron porque este sistema operativo llegó a su fin de vida. Se solucionó redirigiendo los repositorios hacia vault.centos.org directamente en el Dockerfile.
