# Informe — Práctica 2 de Tomcat

## 1. Cabecera

Nombre, fecha, sistema operativo, JDK, versión de Tomcat, método de
publicación elegido y tipo de entorno.

[Responde aqui]

## 2. Objetivo y alcance

Explica el objetivo de la práctica e indica qué partes y ampliaciones has
realizado.

[Responde aqui]

## 3. Arquitectura y recorrido

Incluye un diagrama propio del recorrido cliente → conector → servicio →
motor → host → contexto → Servlet. Explica qué componente produce cada parte
de la respuesta y diferencia el HTML estático de la respuesta generada por un
Servlet.

[Responde aqui]

## 4. Requisitos y recursos

Registra permisos, rutas, puertos, firewall, nombres, cliente de prueba,
compatibilidad entre Java y Tomcat y tipo de entorno utilizado.

[Responde aqui]

## 5. Instalación y servicio

Documenta los comandos utilizados para instalar Java y Tomcat, crear la cuenta
de servicio, configurar `systemd`, arrancar, parar, reiniciar y consultar
Tomcat. Indica el usuario que ejecuta el servicio y las variables
`JAVA_HOME`, `CATALINA_HOME` y `CATALINA_BASE`.

Consulta [la evidencia de la cuenta y la versión](evidencias-tomcat-p2/3.-cuenta-version-y-rutas.txt)
y [la evidencia del servicio](evidencias-tomcat-p2/4.-servicio-systemd.txt).

[Responde aqui]

## 6. Rutas y arquitectura de Tomcat

Explica la función de `bin`, `conf`, `lib`, `webapps`, `logs`, `work` y
`temp`. Indica qué archivos son de configuración y cuáles genera Tomcat.

Consulta [la evidencia de arquitectura](evidencias-tomcat-p2/5.-arquitectura-tomcat.txt).

[Responde aqui]

## 7. Aplicación `saludo-app`

Documenta la estructura de la aplicación, su HTML, Servlet, descriptor
`web.xml`, fuente Java y clase compilada. Indica qué ocurre al enviar un nombre
y qué respuesta se obtiene.

Consulta [la evidencia de saludo](evidencias-tomcat-p2/7.-saludo-app.txt).

[Responde aqui]

## 8. Aplicación `repetidor-app`

Documenta la estructura de la aplicación, su HTML, Servlet, descriptor
`web.xml`, fuente Java y clase compilada. Explica el bucle del servidor y la
validación de cantidades.

Consulta [la evidencia del repetidor](evidencias-tomcat-p2/8.-repetidor-app.txt).

[Responde aqui]

## 9. Compilación, WAR y despliegue

Incluye los comandos de compilación y la versión de `servlet-api.jar`.
Documenta el contenido relevante de los dos WAR, su propiedad, su copia a
Tomcat y la detección o despliegue de las aplicaciones.

Consulta [la evidencia de WAR y despliegue](evidencias-tomcat-p2/9.-war-y-despliegue.txt).

[Responde aqui]

## 10. Conector HTTP y estado

Documenta el `Connector`, el puerto, el socket en escucha, el estado de
`systemd` y la propiedad de los archivos. Explica por qué un servicio activo no
demuestra por sí solo que las aplicaciones funcionen.

Consulta [la evidencia del conector](evidencias-tomcat-p2/6.-conector-http.txt).

[Responde aqui]

## 11. Pruebas HTTP y funcionales

Incluye respuestas `curl` de los dos contextos o nombres, pruebas `POST` de
ambas aplicaciones, pruebas funcionales del navegador y una prueba negativa de
una ruta inexistente. Registra resultado esperado, resultado obtenido y estado.
Interpreta el código `404`.

Consulta las evidencias de [pruebas HTTP del método A](evidencias-tomcat-p2/10.-pruebas-metodoA-http.txt),
[pruebas funcionales](evidencias-tomcat-p2/11.-pruebas-funcionales-metodoA.txt) y
[pruebas HTTP del método B](evidencias-tomcat-p2/13.-pruebas-metodoB-http.txt).

[Responde aqui]

## 12. Publicación y hosts virtuales

Indica el método de publicación elegido y compara el método A y el método B.
Explica la diferencia entre un *context path* y un host virtual, qué
información viaja en la cabecera `Host` y las ventajas e inconvenientes de
cada alternativa. Si has usado hosts virtuales, documenta `server.xml`,
`appBase`, `ROOT` y la resolución de nombres.

Consulta [la configuración del método B](evidencias-tomcat-p2/12.-server.xml-metodoB)
y [sus pruebas](evidencias-tomcat-p2/13.-pruebas-metodoB-http.txt).

[Responde aqui]

## 13. Ampliación con Nginx

Si has realizado esta ampliación, incluye la configuración, la validación, las
respuestas y los registros de Nginx. Explica el recorrido Nginx → Tomcat →
Servlet. Si no la has realizado, indica `N/A`.

[Responde aqui]

## 14. Ampliación con máquina virtual o contenedor

Si has realizado esta ampliación, documenta la imagen o contenedor, digest o
identificador, recursos, red, puertos, logs y procedimiento de parada y
recuperación. Si no la has realizado, indica `N/A`.

[Responde aqui]

## 15. Registros y ciclo de vida

Relaciona las peticiones, despliegues e incidencias con `catalina.out`,
`journalctl` y los registros disponibles. Deja el servicio iniciado y explica
las operaciones de recuperación.

Consulta [los registros y el ciclo de vida](evidencias-tomcat-p2/14.-registros-y-ciclo-vida.txt).

[Responde aqui]

## 16. Matriz de pruebas

Completa una fila por prueba con identificador, precondiciones, origen, acción,
resultado esperado, resultado obtenido, estado (`PASS`, `FAIL`, `BLOCKED` o
`N/A`) y evidencia.

| ID | Precondiciones | Origen | Acción | Resultado esperado | Resultado obtenido | Estado | Evidencia |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

[Responde aqui]

## 17. Ejercicios de análisis

### 17.1. Arquitectura

Explica qué componente produce cada parte de la respuesta y diferencia el HTML
estático de la respuesta del Servlet.

[Responde aqui]

### 17.2. Servidor web y servidor de aplicaciones

Compara Nginx y Tomcat. Indica quién acepta la petición, quién ejecuta Java,
qué componente puede actuar como proxy y por qué un HTML estático no demuestra
lógica de backend.

[Responde aqui]

### 17.3. Jerarquía de Tomcat

Relaciona `Connector`, `Service`, `Engine`, `Host`, `Context` y Servlet con los
archivos o bloques de configuración utilizados.

[Responde aqui]

### 17.4. Estructura web

Inventaría los recursos de cada aplicación: HTML, `web.xml`, fuente Java,
`.class`, `servlet-api.jar`, WAR, carpeta de despliegue y logs. Indica qué se
puede solicitar desde el navegador y qué queda bajo `WEB-INF`.

[Responde aqui]

### 17.5. WAR y contexto

Explica por qué `saludo-app.war` se publica en `/saludo-app/`, qué ocurriría
con `ROOT.war` y por qué el nombre no sustituye a la comprobación del contexto
efectivo.

[Responde aqui]

### 17.6. HTTP

Analiza la salida de `curl --include` de ambas aplicaciones. Identifica el
estado, al menos tres cabeceras, método, puerto, contexto y cuerpo. Explica por
qué un `200` del formulario no demuestra por sí solo que se haya ejecutado el
Servlet correcto.

[Responde aqui]

### 17.7. Comparación de publicación

Compara el método A y el método B. Explica qué diferencia un contexto de un
host virtual, qué información viaja en `Host` y las ventajas e inconvenientes
de cada alternativa.

[Responde aqui]

### 17.8. Diagnóstico

Documenta una incidencia reversible, predice el resultado, conserva el primer
fallo y explica qué log y qué prueba permiten localizarlo. Restaura el servicio
al terminar.

[Responde aqui]

### 17.9. Compatibilidad

Explica por qué `jakarta.servlet.*` es necesario con Tomcat 10.1 y qué problema
aparecería al trasladar sin cambios una aplicación compilada para
`javax.servlet.*`.

[Responde aqui]

### 17.10. Seguridad y mantenimiento

Explica por qué Tomcat no debe ejecutarse como `root`, por qué no se deben
publicar `tomcat-users.xml` ni credenciales, qué diferencia hay entre `conf` y
`work` y qué copia de recuperación conservarías antes de editar `server.xml`.

[Responde aqui]

### 17.11. Entornos aislados

Si realizas la ampliación de VM o Docker, compara el puerto interno con el
puerto publicado y explica qué evidencia demuestra el funcionamiento del
entorno. Si no la realizas, indica `N/A`.

[Responde aqui]

### 17.12. Evidencias y criterios

Relaciona cada evidencia del informe con los criterios RA1.a, RA1.b, RA1.d,
RA1.f, RA1.g, RA1.h y RA1.i. Marca `PASS`, `FAIL`, `BLOCKED` o `N/A`.

[Responde aqui]

## 18. Incidencias y recuperación

Describe las incidencias encontradas, su causa, la solución aplicada, la
prueba de cierre, el procedimiento de detención y la forma de repetir o
revertir el laboratorio. Incluye la copia de seguridad de `server.xml`.

[Responde aqui]

## 19. Fuentes y fecha de validación

Relaciona las fuentes consultadas y la fecha de validación de la documentación.

[Responde aqui]
