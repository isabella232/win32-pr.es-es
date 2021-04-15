---
description: Conceptos básicos de DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Conceptos básicos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d0b2af8bc16fa0890c0103a063e750364cece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677151"
---
# <a name="dvd-basics"></a>Conceptos básicos de DVD

Las características que hacen que el DVD sea atractivo para los consumidores (bifurcación perfecta, varios idiomas, control parental, compatibilidad con karaoke y varios ángulos) también hacen que el trabajo del desarrollador sea un poco más complejo. Un reproductor de DVD no solo debe reproducir secuencias de audio, vídeo y subimágenes, sino que también debe realizar un seguimiento de las opciones de navegación que el disco está permitiendo actualmente y administrar correctamente muchos tipos de comandos de usuario. El navegador de DVD le protege de gran parte de esta complejidad, al tiempo que permite crear una aplicación de DVD totalmente funcional. No es necesario hacer referencia a la especificación de DVD para usar la API del explorador de DVD de forma eficaz, pero sí es necesario conocer los conceptos básicos de navegación en DVD.

**Datos de control de navegación**

Los datos de audio y vídeo de un disco DVD-Video se intercalan a intervalos regulares con varios tipos de datos de control de navegación. Estos datos pueden ser una instrucción que indica al reproductor que haga algo, por ejemplo, si se mueve a algún lugar determinado del disco, o puede tratarse de un marcador de solo informativo que informa al reproductor por ejemplo de que el contenido que sigue tiene un nivel superior de administración parental que el contenido anterior, o que la operación de omisión del capítulo está deshabilitada. El reproductor retransmite esta información a una aplicación y es responsabilidad de la aplicación actuar sobre ella. Estos marcadores de navegación forman parte de lo que ofrece a DVD su mayor nivel de interactividad de usuario en comparación con los CDs de vídeo. Una aplicación de reproductor de DVD debe controlar los eventos que se originan en el disco, así como los eventos que se originan con el usuario.

**Datos de audio, vídeo y subimagen**

Un disco DVD-Video contiene tres tipos principales de secuencias: vídeo, audio y subimagen.

-   El flujo de vídeo puede contener hasta nueve "ángulos", que se pueden considerar como subflujos. Los autores de DVD pueden incluir varios ángulos dondequiera que deseen ofrecer al visor una selección de ángulos de cámara desde los que ver la misma escena. Solo puede haber un ángulo activo a la vez. La secuencia de vídeo también contiene datos de subtítulos de línea 21, si existen.
-   Puede haber hasta ocho flujos de audio independientes, o pistas, que proporcionan hasta ocho bandas sonoras multicanal y permiten que los discos de Karaoke de DVD usen audio multicanal.
-   Un DVD puede contener hasta 32 secuencias de *subimágenes* . Constan de mapas de bits comprimidos de 16 colores con un canal alfa, que se superponen encima del vídeo. Normalmente, las secuencias de subimagen contienen subtítulos y botones de menú, aunque también pueden contener otros gráficos. Un flujo de subimagen puede tener un idioma especificado. Siempre se muestra el contenido de la subimagen y el contenido de la subimagen solo se muestra si el usuario lo habilita.

Tenga en cuenta que los títulos de una secuencia de subimagen no son los mismos que los subtítulos (CC) de línea 21. Los subtítulos (CC), que están destinados a visores difíciles de oír, se insertan en la señal de vídeo. Están formadas por completo de cadenas de caracteres. Por otro lado, las leyendas de subimagen son mapas de bits gráficos. En un dispositivo de consumidor, los subtítulos se muestran en el conjunto de televisión, mientras que el flujo de subimagen se representa mediante el reproductor de DVD. Un DVD puede contener ambos tipos de título.

**Títulos y capítulos**

El contenido de vídeo de un DVD se divide en *títulos* y *menús*. Los títulos se dividen en unidades que la especificación de DVD llama a *partes de los títulos* (PTTs). Con mayor frecuencia, se denominan *escenas* o *capítulos*. (La documentación de DirectShow usa el término capítulo). El visor puede navegar a títulos o capítulos específicos de los títulos.

El autor de un DVD decide cómo dividir el contenido en títulos y capítulos. Cuando un DVD contiene una película de longitud de característica, a menudo se coloca en un título la película completa, dividida en capítulos para cada escena. Las características adicionales del DVD, como finalizadores o escenas eliminadas, se colocan en títulos independientes. Sin embargo, estas divisiones son arbitrarias y muchos DVDs se organizan de forma diferente.

Puede haber hasta 99 títulos en un disco y los autores del disco pueden dividir el título en un máximo de 999 capítulos lógicos. En la mayoría de las películas de características de DVD, el contenido de la película tiene el formato de una serie de capítulos que se reproducen uno tras otro. En estos discos, el marcador de final de segmento contiene una instrucción de bifurcación que indica al reproductor que continúe reproduciendo el siguiente capítulo de la secuencia. Estos títulos se conocen como *un título de PGC secuencial*. (PGC representa la cadena de programas, otro nombre para un grupo de capítulos que pertenecen a la vez. Este término no se utiliza en la documentación del navegador de DVD). En los discos con otros tipos de contenido, como los discos de karaoke, un marcador de fin de capítulo podría indicar al reproductor que muestre un menú o simplemente indicar al reproductor que se detenga.

Los desarrolladores de aplicaciones de DVD utilizan los números de título y de capítulo para saltar a puntos específicos de un disco. Para obtener un acceso más preciso, se puede usar un número de título y un código de tiempo. Los códigos de tiempo solo se pueden usar con un título de PGC secuencial, ya que otros tipos no contienen mapas de código de tiempo.

**Menús**

La especificación de DVD define seis tipos de menús:

-   **Titulo.** El menú de título es el primer menú que se va a mostrar. Normalmente, tiene botones para seleccionar títulos. El menú de título también se denomina *menú administrador de vídeos*. Solo hay un menú de título en un DVD.
-   **Raíces.** Un menú raíz es el menú de nivel superior de un título. Cada título puede tener un menú raíz. Los cuatro menús siguientes son submenús del menú raíz. Un menú raíz también se denomina *menú de conjunto de títulos de vídeo*. Normalmente, el menú raíz tiene botones que navegan a cualquiera de los títulos del conjunto de títulos. Además, puede tener submenús que permitan al usuario elegir opciones para la secuencia de audio, el ángulo de la cámara, la secuencia de subimagen o el capítulo. Sin embargo, estos submenús no se usan en la mayoría de los DVDs.
-   **Subimagen.** El menú de subimagen selecciona la secuencia de subimagen.
-   **Audio.** El menú audio selecciona la secuencia de audio. Normalmente, este menú permite al visor seleccionar una pista de idioma.
-   **Angulo.** El menú de ángulo selecciona el ángulo de la cámara.
-   **Capítulo.** En el menú de capítulo, también denominado menú PTT, se seleccionan los capítulos de un título.

La mayoría de los menús tienen botones, que se pueden *seleccionar* y *Activar*. Al seleccionar un botón se cambia la apariencia del botón. Al activar un botón, se desencadena un comando de DVD, como mostrar otro menú o iniciar la reproducción.

**Niveles de administración parental**

Todo o parte de un disco DVD se puede codificar con un nivel de administración parental (PML) numerado de uno a ocho. Ocho es el nivel más restrictivo (solo para adultos) y uno es el menos restrictivo (todas las edades). La idea es evitar que los niños vean contenido para adultos sin consentimiento parental, al tiempo que permite a los adultos ver contenido seguro para niños. En el Estados Unidos y Canadá, los niveles se asignan al sistema de clasificación de MPAA (G, PG, PG-13, NC-17), pero este no es el caso en otros países o regiones.

Dado que los capítulos pueden existir lógicamente dentro de un bloque parental, puede haber dos versiones del mismo capítulo en un título, cada una de las cuales asigna un PML diferente y en un bloque parental diferente. Por ejemplo, un elemento secundario que inicia sesión y reproduce el disco verá una versión del capítulo 3, y un adulto que inicie sesión verá una versión diferente, suponiendo que la aplicación admita PMLs.

Un título o un capítulo también puede contener PMLs temporales, cuyo contenido se clasifica por encima del valor de PML para el título o el capítulo en su conjunto. Esto significa que un título puede tener más de un nivel parental. Los PMLs temporales normalmente se crean como bloques de ángulo, de modo que una escena de una película puede tener dos versiones, una clasificada por visores jóvenes y otra para adultos.

Es responsabilidad de la aplicación del reproductor aplicar los niveles parentales.

**Dominios**

El término *dominio* hace referencia al estado interno de un reproductor de DVD; no se crea nada en el disco. Los dominios son importantes porque algunos comandos de DVD solo son válidos en determinados dominios. DirectShow proporciona una manera de consultar el dominio actual y recibir una notificación cuando cambia el dominio. Se definen los siguientes dominios:

-   **Primer juego.** En este dominio, el reproductor de DVD acaba de empezar a reproducir el DVD. Una vez que entra en el primer dominio de reproducción, el reproductor cambia a otro dominio, ya sea un dominio de menú o el dominio de título, según el disco.
-   **Menú del administrador de vídeo.** El reproductor muestra el menú del administrador de vídeo, también denominado menú de título.
-   **Menú VTS.** El reproductor muestra un menú asociado a un conjunto de títulos de vídeo, ya sea el menú raíz o un submenú (audio, subimagen, ángulo o capítulo).
-   **Titulo.** El reproductor está reproduciendo vídeo en un título.
-   **Detener.** El reproductor no muestra nada. (En realidad, la especificación de DVD no llama a este estado un dominio, pero se puede tratar como uno).

El dominio puede considerarse como una variable de estado que un reproductor de DVD supervisa, con el fin de realizar un seguimiento del tipo de contenido que el reproductor está leyendo actualmente en el disco. los reproductores de DVD usan dominios para evitar la emisión de comandos sin sentido a la unidad de DVD.

**Controles de operación de usuario**

Los controles de operación de usuario (UOPs) son marcadores en un disco que los autores de DVD pueden insertar en cualquier parte para restringir las opciones de navegación de un usuario. La mayoría de los discos siguen las restricciones de UOP estándar. Por ejemplo, la mayoría de los discos no permiten que el visor avance rápido ni muestre un menú en el primer dominio de reproducción. En principio, cada disco puede insertar cualquier comando de UOP en cualquier punto del disco, aunque el comando sea válido en el dominio actual. Por ejemplo, se puede crear un disco para no permitir el reenvío rápido en un determinado título o para impedir que se muestre un menú determinado después de que el usuario escriba el dominio de título. El navegador de DVD es compatible con todos estos comandos del disco y no permitirá que una aplicación invalide los controles UOP del disco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



