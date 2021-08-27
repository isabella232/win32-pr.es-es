---
description: Conceptos básicos de DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Conceptos básicos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a61299c4c0d3e83235a741c262efae685aa74ffa525aa08f9cf9a2e58b957e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102945"
---
# <a name="dvd-basics"></a>Conceptos básicos de DVD

Las características que hacen que el DVD sea atractivo para los consumidores (bifurcación sin problemas, varios idiomas, control parental, compatibilidad con el lenguaje y varios ángulos) también hacen que el trabajo del desarrollador sea un poco más complejo. Un reproductor de DVD no solo debe reproducir secuencias de audio, vídeo y subpicture, sino que también debe realizar un seguimiento de las opciones de navegación que el disco permite actualmente y controlar correctamente muchos tipos de comandos de usuario. El navegador de DVD le protege de gran parte de esta complejidad a la vez que le permite crear una aplicación de DVD totalmente funcional. No es necesario hacer referencia a la especificación de DVD para usar la API DVD Navigator de forma eficaz, pero es necesario conocer los conceptos básicos de navegación de DVD.

**Datos del control de navegación**

Los datos de audio y vídeo de DVD-Video disco se intercalan a intervalos regulares con varios tipos de datos de control de navegación. Estos datos pueden ser una instrucción que indica al jugador que haga algo, por ejemplo, moverse a un lugar determinado del disco, o puede ser un marcador de solo información que informa al jugador, por ejemplo, que el contenido que sigue tiene un nivel de administración parental superior al contenido anterior, o que la operación de skip del capítulo está deshabilitada. El reproductor retransmite esta información a una aplicación y es responsabilidad de la aplicación actuar sobre ella. Estos marcadores de navegación forman parte de lo que da a DVD su mayor nivel de interactividad del usuario en comparación con los CDs de vídeo. Una aplicación de reproductor de DVD debe controlar los eventos que se originan con el disco, así como los eventos que se originan con el usuario.

**Datos de audio, vídeo y subimagen**

Un DVD-Video disco contiene tres tipos principales de secuencias: vídeo, audio y subimagen.

-   La secuencia de vídeo puede contener hasta nueve "ángulos", que se pueden pensar como substreams. Los autores de DVD pueden incluir varios ángulos donde deseen ofrecer al visor una selección de ángulos de cámara desde los que ver la misma escena. Solo un ángulo puede estar activo a la vez. La secuencia de vídeo también contiene datos de subtítulos de línea 21, si existe alguno.
-   Puede haber hasta ocho secuencias de audio independientes, o pistas, que proporcionan hasta ocho canalizaciones multicanal y permiten que los discos DVD dvd puedan usar audio multicanal.
-   Un DVD puede contener hasta 32 *secuencias de subimagen.* Se componen de mapas de bits comprimidos de 16 colores con un canal alfa, que se superponen en la parte superior del vídeo. Normalmente, las secuencias de subimagen contienen subtítulos y botones de menú, aunque también pueden contener otros gráficos. Una secuencia de subimagen puede tener un idioma especificado. Siempre se muestra algún contenido de subimagen y algún contenido de subimagen solo si el usuario lo habilita.

Tenga en cuenta que los títulos de una secuencia de subimagen no son los mismos que los subtítulos de línea 21. Los subtítulos, que están diseñados para visores con dificultades auditivas, se insertan en la señal de vídeo. Constan completamente de cadenas de caracteres. Por otro lado, los subtítulos son mapas de bits gráficos. En un dispositivo de consumidor, el conjunto de televisión muestra los subtítulos, mientras que el reproductor de DVD representa la secuencia de subaspección. Un DVD puede contener ambos tipos de título.

**Títulos y capítulos**

El contenido de vídeo de un DVD se divide *en títulos* *y menús.* Los títulos se dividen en unidades a las que la especificación de DVD llama *a partes de títulos* (PT). Más a menudo, se *denominan escenas* o *capítulos.* (En la DirectShow se usa el término capítulo). El visor puede navegar a títulos o capítulos específicos dentro de los títulos.

El autor de un DVD decide cómo dividir el contenido en títulos y capítulos. Cuando un DVD contiene una película de longitud de características, la película completa a menudo se coloca en un título, dividido en capítulos para las escenas individuales. Las características adicionales del DVD, como los finalizadores o las escenas eliminadas, se colocan en títulos independientes. Sin embargo, estas divisiones son arbitrarias y muchos DVD se organizan de forma diferente.

Puede haber hasta 99 títulos en un disco y los autores de discos pueden dividir el título en hasta 999 capítulos lógicos. En la mayoría de las características de DVD, el contenido de la película tiene el formato de una serie de capítulos que se reproducen automáticamente una tras otra. En estos discos, el marcador de final de capítulo contiene una instrucción de bifurcación que indica al reproductor que siga reproduciendo el siguiente capítulo de la secuencia. Estos títulos se conocen como títulos *PGC secuenciales.* (PGC significa cadena de programas, otro nombre para un grupo de capítulos que pertenecen juntos. Este término no se usa en la documentación de DVD Navigator). En discos con otros tipos de contenido, como discos de vídeo, un marcador de fin de capítulo podría indicar al reproductor que muestre un menú o simplemente indicar al reproductor que se detenga.

Los desarrolladores de aplicaciones de DVD usan números de título y capítulo para saltar a puntos específicos de un disco. Para un acceso más fino, se puede usar un número de título y un código de hora. Los códigos de tiempo solo se pueden usar con títulos PGC secuenciales, ya que otros tipos no contienen mapas de código de tiempo.

**Menús**

La especificación de DVD define seis tipos de menú:

-   **Título.** El menú título es el primer menú que se muestra. Normalmente tiene botones para seleccionar títulos. El menú título también se denomina menú *administrador de vídeo*. Solo hay un menú de título en un DVD.
-   **Raíz.** Un menú raíz es el menú de nivel superior de un título. Cada título puede tener un menú raíz. Los cuatro menús siguientes son submenús del menú raíz. Un menú raíz también se denomina menú *de conjunto de títulos de vídeo.* Normalmente, el menú raíz tiene botones que navegan a cualquiera de los títulos del conjunto de títulos. Además, puede tener submenús que permiten al usuario elegir opciones para la secuencia de audio, el ángulo de la cámara, la secuencia de subimagen o el capítulo. Sin embargo, estos submenús no se usan en la mayoría de los DVD.
-   **Subimagen.** El menú de subpicture selecciona la secuencia de subimagen.
-   **Audio.** El menú de audio selecciona la secuencia de audio. Normalmente, este menú permite al visor seleccionar una pista de idioma.
-   **Ángulo.** El menú angular selecciona el ángulo de la cámara.
-   **Capítulo.** El menú de capítulos, también denominado menú PTT, selecciona capítulos dentro de un título.

La mayoría de los menús tienen botones, que se *pueden seleccionar y* *activar.* Al seleccionar un botón se cambia la apariencia del botón. La activación de un botón desencadena un comando de DVD, como mostrar otro menú o iniciar la reproducción.

**Niveles de administración parental**

Todo o parte de un disco de DVD se puede codificar con un nivel de administración parental (PML) numerado de uno a ocho. Ocho es el nivel más restrictivo (solo adultos) y el menos restrictivo (todas las edades). La idea es evitar que los niños vean contenido para adultos sin consentimiento parental, al tiempo que se permite a los adultos ver contenido seguro para los niños. En Estados Unidos y Canadá, los niveles se asignan al sistema de clasificación de MPAA (G, PG, PG-13, NC-17), pero esto no es así en otros países o regiones.

Dado que los capítulos pueden existir lógicamente dentro de un bloque parental, puede haber dos versiones del mismo capítulo en un título, cada una asignada a una PML diferente y en un bloque parental diferente. Por ejemplo, un elemento secundario que inicia sesión y reproduce el disco vería una versión del capítulo 3 y un adultos que inicia sesión vería una versión diferente, suponiendo que la aplicación admite LAS PML.

Un título o capítulo también puede contener PML temporales, cuyo contenido se clasifica por encima de la PML para el título o el capítulo en su conjunto. Esto significa que un título puede tener más de un nivel parental. Las PML temporales se suelen crear como bloques angulares, de modo que una escena de una película puede tener dos versiones, una clasificada para espectadores más pequeños y otra para adultos.

Es responsabilidad de la aplicación player aplicar los niveles parentales.

**Dominios**

El término *dominio* hace referencia al estado interno de un reproductor de DVD; no es algo que se cree en el disco. Los dominios son importantes porque algunos comandos de DVD solo son válidos en determinados dominios. DirectShow proporciona una manera de consultar el dominio actual y recibir una notificación cuando cambia el dominio. Se definen los siguientes dominios:

-   **Primera reproducción.** En este dominio, el reproductor de DVD acaba de empezar a reproducir el DVD. Después de entrar en el dominio First Play, el reproductor cambia a otro dominio, ya sea un dominio de menú o el dominio de título, según el disco.
-   **Menú administrador de vídeo.** El reproductor muestra el menú Administrador de vídeo, también denominado menú de título.
-   **Menú VTS.** El reproductor muestra un menú asociado a un conjunto de títulos de vídeo, ya sea el menú raíz o un submenú (audio, sub picture, ángulo o capítulo).
-   **Título.** El reproductor está reproduciendo vídeo en un título.
-   **Parada.** El reproductor no muestra nada. (Estrictamente hablando, la especificación de DVD no llama a este estado un dominio, pero se puede tratar como uno).

El dominio se puede pensar en como una variable de estado que supervisa un reproductor de DVD, con el fin de realizar un seguimiento del tipo de contenido que el reproductor está leyendo actualmente desde el disco. Los reproductores de DVD usan dominios para evitar emitir comandos sin sentido a la unidad de DVD.

**Controles de operación de usuario**

Los controles de operación de usuario (UOP) son marcadores en un disco que los autores de DVD pueden insertar en cualquier lugar para restringir las opciones de navegación de un usuario. La mayoría de los discos siguen las restricciones estándar de UOP. Por ejemplo, la mayoría de los discos no permiten al visor avanzar rápidamente o mostrar un menú mientras está en el dominio De primera reproducción. En principio, cada disco puede insertar cualquier comando UOP en cualquier punto del disco, incluso si el comando sería válido en el dominio actual. Por ejemplo, se puede crear un disco para no permitir el reenvío rápido en un título determinado o para evitar que se muestra un menú determinado después de que el usuario entra en el dominio de título. El navegador de DVD cumple con todos estos comandos del disco y no permitirá que una aplicación invalide los controles UOP del disco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



