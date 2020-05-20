# TP Backend 2020

## :bookmark_tabs: Flashcard APP :bookmark_tabs:

### :small_orange_diamond: Idea principal

Se desea desarrollar una aplicación que tenga como objetivo facilitar el estudio, basándose para ello en la metodología de [flashcards](https://es.wikipedia.org/wiki/Flash_cards).

### :small_orange_diamond: Propósito

Tomando en cuenta dicho método de estudio y analizando las diferentes alternativas que se encuentran ya disponibles, se llegó a la conclusión de que estas aplicaciones ya existentes carecen de algunas características importantes y/o no otorgan una interfaz pulida, cómodo y útil para el usuario.

Se decidió entonces desarrollar una aplicación propia que incluya todas estas características importantes de la metodología y poner especial énfasis en la interfaz y experiencia de usuario.

Además, la relativa sencillez del proyecto permitirá una vez desarrolladas las características principales, poder llevarlo a producción de manera rápida, propiciando así, una utilidad real y clara de la idea en cuestión.

### :small_orange_diamond: Breve descripción del proyecto

Una vez registrado en la web, el usuario tiene la posibilidad de crear **temáticas de estudio** (ej: 1° Parcial teórico de TTADS, Final de SO, etc).

Creada una temática, procede a crear **flashcards** para la misma:

Escribe el lado A de la tarjeta, y su correspondiente respuesta en el lado B. Se espera que la tarjeta sea personalizable, incluyendo poder elegir el estilo de la misma, color, poder añadir imágenes, links, dibujar sobre ella, etc. ***

Además de este tipo de tarjeta "simple", el usuario también podrá añadir otros tipos de tarjetas como:

  * Tarjetas de verdadero o falso
  * Tarjetas de multiple choice ***
  * Tarjetas de ordenar los pasos ***
  * Tarjetas de unir con flechas ***

Una vez finalizada la creación de todas ellas, y llegado el momento de "estudio", el usuario seleccionará la temática a repasar. La web le irá mostrando el lado A de las tarjetas de dicha temática, y este deberá pensar la respuesta a la pregunta, corroborando su saber con el lado B.

Si considera que su respuesta ha sido correcta tildará la opción de **LO SABÍA**, o **ESTABA EQUIVOCADO** en el caso contrario. Si las tarjetas son de los otros tipos listados, la web decidirá ella misma si acertó o no.

Finalmente el usuario podrá ver **estadísticas** de cada temática, cuales respuestas acierta más y cuales menos, su porcentaje de acierto a lo largo del tiempo y otras estadísticas de interés.

Se espera que dichas estadísticas sirvan como input del sistema para modificar las tarjetas que va mostrando de forma sucesiva al usuario y así lograr un aprendizaje más eficiente. ***

Requisitos a considerar:

  * Exportar flashcards a formato PDF para así poder imprimirlas o usarlas. ***
  * Compartir Flashcards con otros usuarios: las temáticas tendrían el atributo **privado**, o **público**. En el caso de que sean públicas, otro usuario, mediante un link, podría clonar todas las flashcards a su cuenta y así poder modificarlas o agregar otras nuevas. ***
  *Las temáticas podrían ser además, **colaborativas**, para otros usuarios, mediante un link de invitación. ***

> *** Según la complejidad de algunas de estas características, las mismas no serían añadidas en una primera instancia.

### :small_orange_diamond: Tecnologías

El proyecto exige poner una gran atención al frontend de la aplicación. La idea es la de desarrollar una **SPA** y que la misma pueda ser exportada luego (mediante un Serice Worker o ya sea de forma empaquetada) a dispositivos móviles como así también a desktop (Serice Worker, o Electron) y poder otorgar funcionalidades offline.

Se elige **VUE** para el framework frontend y **NodeJS** para su correspondiente backend.
Se considera que la base de datos hecha en **MongoDB**, dado a su naturaleza noSQL es idónea para almacenar los datos de cada una de las flashcards y como así también de toda la aplicación.


### :small_orange_diamond: ABMC

Se listan algunos ABMC principales:

  * *ABMC de Usuario*
  * *ABMC de Temáticas*
  * *ABMC de Flashcards*

### :small_orange_diamond: Listados

  * *Listar Temáticas*
  * *Listar Flashcards*

### :small_orange_diamond: Modelo de Dominio

![Modelo_de_Dominio](https://i.imgur.com/ZgceeaE.png)


### :small_orange_diamond: Repositorio

* [motiontx/flashcards-app](https://github.com/motiontx/flashcards-app)


### :small_orange_diamond: Integrantes

  * Vittorio Retrivi - 44727 >> [:octocat:](https://github.com/motiontx)

---

## 1 - Enunciado

### 1.1 - Desarrollo

Desarrollar un backend utilizando una API REST o GraphQL y un frontend parcial con las siguientes caracterísitcas:

  * El backend debe ser programado en JavaScript con NodeJS.
  * Debe utilizar un framework/middleware. Se dará soporte sobre Express pero podrán utilizarse alternativas si así se prefiere.
  * La persistencia debe realizarse utilizando un ODM/ORM con una base de datos persistente acorde a la tecnología que se utilice.
  * El frontend debe realizarse con un framework como Angular u otro seleccionado, html 5 y para CSS debe usarse un preprocessador o framework.
  * El tema y alcance del trabajo debe ser propuesto por los alumnos y aprobado por los docentes de la cátedra (o utilizar el del año 2017)

### 1.2 - Funcionalidad
Ver [checklist]
#### 1.2.1 - Backend por API REST o GraphQL

  * ABMC:
      * ABMC de entidad simple (no depende de otras entidades) por API. *Al menos 1 por integrante*

      * ABMC de una entidad que requiera de otra ya existente de la que se hizo ABMC en el item anterior. Ej: ABMC de articulos donde un atributo sea la categoría que a su vez es una entidad con ABMC.  *Grupos de 1 o 2 miembros: al menos 1. Grupos de 3 y 4 miembros: 2 o más*

      * Otros ABMC que exedan el mínimo requerido pueden hacerse manualmente por base de datos o por API. Si se hacen por API suman nota adicional. Sólo se considerarán el doble de ABMCs

  * Listados por API:
      * Listado simple: al menos uno de las entidades creadas por API. *Al menos 1 listado sin importar la cantidad de integrantes*
      * Listado complejo:

        *Grupos de hasta 2 integrantes: al menos 1 listado complejo. Grupos de 3 y 4 miembros: 2 listados complejos de cualquier opción.*
        * Opción 1: debe incluir datos de al menos dos entidades.
        * Opción 2: el listado debe permitir filtrar por al menos 1 atributo.

      * Sólo se considerarán listados complejos con filtros de uno o más atributos para nota adicional.

  * Detalle:
    * Presentar un detalle por API de alguno de los elementos en un listado
    * Al realizar el request se debe utilizar un ID u otro identificador obtenido de un elemento del listado, deberán devolverse más datos sobre el mismo que los que figuran en el listado.
    * El mismo debe proveer información de dos o más entidades relacionadas. La información adicional debe ser acorde al tipo de API (REST o GraphQL) utilizada.

    *Grupos de 1 o 2 integrates, al menos 1.
    Grupos de 3 y 4 integrantes al menos 2.
    Dos detalles básicos pueden ser reemplazados por 1 detalle parametrizable*

    * Sólo se considerarán para nota adicional detalles que no coincidan con ABMCs creados.


  * Otros: En caso de querer implementar otros elementos en reemplazo o adición a los requeridos pactar con los docentes primero.

#### 1.2.2 - Frontend

  * El frontend al menos deberá permitir invocar a la API y mostrar los resultados de uno de los listados. Haciendo click en un elemento del listado (o parte de él) debe mostrar el detalle correspondiente a un elemento de dicho listado invocando a una API del listado creada para el backend.

  * El resto de la funcionalidad puede utilizarse mediante una herramienta similar a postman, restclient, curl o wget.

  * No se considerará trabajo adicional en el frontend para sumar nota ya que hay un TP dedicado a ello.

## 2 - Alcance y Entregas
### 2.1 - Definición de Alcance

El equipo deberá definir el alcance del trabajo práctico con el equipo docente. Indicando los criterios de aceptación.

Las mismas podrán volverse a pactar con los profesores enviando las correcciones a la misma indicando, causas, acciones correctivas que se tomarán.

En caso de realizar cambios sobre el alcance deberá dejarse una copia de la versión pactada original dentro del repositorio.

### 2.2 - Entrega Inicial

Para iniciar el proyecto deberá crear un fork de este repositorio.
Editar el README.md para incluir:

En el readme de dicho repo debe figurar:
  * Enunciado general del tp.
  * Indicado una breve descripción para cada item requerido.
    * ABMC: nombre de la entidad y atributos.
    * Listado: breve descripción del listado (1 línea), tipo (simple, complejo)
    * Detalle: entidades involucradas y, si corresponde, los parámetros.
  * Miembros del equipo indicando, legajo, nombre y apellido.
  * Modelo de dominio o modelo de datos. Una imagen referenciada.

Enviar por mail y telegram al profesor la URL del repositorio git para validar el alcance. Esperar la autorización del enunciado. Una vez hecho esto puede comenzar el desarrollo del mismo.

Recuerde revisar el [checklist]

### 2.3 - Entrega Final

  Para realizar la entrega deberá en primer lugar crearse un tag en el repositori de git.

  La entrega final deberá hacerse enviando por email y telegram a los profesores la URL del tag de git.

  Pactar con el docente un fecha para la defensa.


## 3 - Criterio de correccion

### 3.1 - Código
  * Diseño adecuado de la API.
  * Diseño del modelo de datos adecuado.
  * Usabilidad del sitio: debe ser fácil de usar, elegante y no tener contenido oculto o difícil de acceder
  * Diseño adecuado de la interfaz: uso apropiado de los tags html y de los estilos, ya sea utilizando un FW CSS o un preprocesador.
  * Calidad del código: uso adecuado de las características del FW y de la API.
  * Completitud de los requerimientos.

### 3.2 - Repositorio
  * El desarrollo deberá realizarse en una plataforma de git gratuita. Se recomienda GitHub o GitLab.
  * Se evaluará el uso de git: Frecuencia y responsables de los commits, uso de branches y merge.

### 3.3 - Defensa

Todos los miembros del grupo deberán aprobar una defensa del código y funcionalidad del TP con los profesores.

Si algún miembro no puede realizar la defensa correspondiente la misma no se considerará aprobada.

Luego de la defensa el resultado puede ser:
* Desarrollo aprobado - Defensa aprobada: se considerará el TP aprobado y se definirá una nota.
* Desarrollo a revisión - Defensa aprobada: se considera aprobada la defensa y se indicarán cambios a realizar en el código. En este caso deberá corregirse el código y enviarse un nuevo tag con las correcciones indicadas en un plazo acordado con el docente. No deberá repetirse la defensa.
* Desarrollo aprobado - Defensa a repetir: se considera el código adecuado y aprobado. Deberá repetirse la defensa en un plazo acordado con el docente.
* Desarrollo a revisión - Defensa a repetir: se pactará una nueva fecha de entrega y defensa con el docente.

[checklist]: ./checklist/README.md
