---
description: A continuación se muestra una lista de glifos de gestos que Microsoft planea admitir en el futuro como parte del reconocedor de gestos de Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifos no implementados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275360"
---
# <a name="unimplemented-glyphs"></a>Glifos no implementados

A continuación se muestra una lista de glifos de gestos que Microsoft planea admitir en el futuro como parte del *reconocedor de gestos de Microsoft*. El trabajo está en curso para asegurarse de que la precisión de reconocimiento de estos glifos es alta (para evitar la activación accidental) y que se asignan a las operaciones adecuadas.

Para garantizar la coherencia de los *gestos* que se usan para *las acciones* comunes entre las aplicaciones, debe cumplir las sugerencias siguientes:

-   La *acción* es el comportamiento semántico sugerido asociado con el gesto.
-   En el caso de los gestos etiquetados como *fijos* en la tabla siguiente, se recomienda no cambiar el comportamiento semántico sugerido. Si una aplicación no necesita el comportamiento semántico especificado, se recomienda que no reutilice el gesto para otra acción o semántica.
-   Debe tener la libertad de asociar comportamientos semánticos relevantes a todos los demás gestos. Estos gestos se etiquetan como *específicos de la aplicación*. En el caso de los gestos que tienen un comportamiento semántico sugerido, se recomienda usar el gesto para la semántica sugerida si la funcionalidad correspondiente existe en la aplicación.
-   El punto de conexión de un gesto es un punto distintivo en la geometría del gesto. El punto de acceso directo se puede usar para determinar dónde se realizó el gesto. La API de gestos permite determinar el punto de acceso frecuente para un gesto determinado. Sin embargo, no todos los gestos tienen un punto de acceso distintivo específico. Para aquellos que no tengan un punto de acceso distintivo determinado, el punto inicial se informará como el punto de acceso frecuente.

> [!Note]  
> Algunos de los gestos tienen un punto de conexión distintiva que simplemente es el punto de partida. Se distinguen en la tabla.

 



| Nombre del gesto                      | Acción                                         | Fijo                           | Punto de acceso frecuente                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinity<br/>               | Activar y desactivar el modo de gesto<br/> | Fijo<br/>                | Punto de partida<br/>                                           |
| Cross<br/>                  | Eliminar<br/>                              | Específico de la aplicación<br/> | Intersección de los trazos<br/>                              |
| Marca de párrafo<br/>         | Nuevo párrafo<br/>                       | Fijo<br/>                | Punto de partida<br/>                                           |
| Sección<br/>                | Nueva sección<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Viñeta<br/>                 | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Viñeta-Cross<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Raya<br/>               | Bold<br/>                                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Swap<br/>                   | Contenido de Exchange<br/>                    | Específico de la aplicación<br/> | Medio del trazo hacia arriba<br/>                                  |
| Openup<br/>                 | Abrir espacio entre palabras<br/>         | Específico de la aplicación<br/> | Mitad del trazo hacia abajo<br/>                                |
| Primer plano<br/>                | Cerrar espacio adicional<br/>                | Específico de la aplicación<br/> | Centro del espacio vertical entre los dos paréntesis<br/> |
| Rectángulo<br/>              | Selecciona el contenido delimitado<br/>            | Fijo<br/>                | Punto de partida<br/>                                           |
| Círculo: Puntee<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Pulsar<br/>                                                      |
| Círculo: círculo<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo-cruzado<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo-línea-vertical<br/>   | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo-línea-horizontal<br/> | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Doble flecha arriba<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Doble flecha abajo<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Doble flecha izquierda<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Doble flecha a la derecha<br/>     | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Arriba-Flecha izquierda<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Arriba-Flecha-derecha<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha abajo a la izquierda<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha abajo a la derecha<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha izquierda<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | El vértice de la punta de la flecha<br/>                               |
| Flecha izquierda hacia abajo<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha a la derecha<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha a la derecha<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Diagonal: leftup<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal: rightup<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal: leftdown<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal: rightdown<br/>     | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-A<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-B<br/>         | Bold<br/>                                | Fijo<br/>                | Punto de partida<br/>                                           |
| Letra latina-C<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-D<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-E<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-F<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-G<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-H<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-I<br/>         | Cursiva<br/>                              | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-J<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-K<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-L<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-M<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-N<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-O<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-P<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-Q<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-R<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-S<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-T<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-U<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-V<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-W<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-X<br/>         | Cortar<br/>                                 | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-Y<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Letra latina-Z<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-0<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-1<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-2<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-3<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-4<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-5<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-6<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-7<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-8<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito-9<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Signo de interrogación<br/>          | Ayuda<br/>                                | Fijo<br/>                | Centrar a lo largo del alto de la curva<br/>                     |
| Sostenido<br/>                  | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Estadounidense<br/>                 | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Asterisk<br/>               | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Center<br/>                                                   |
| Plus<br/>                   | Pegar<br/>                               | Fijo<br/>                | Intersección de los trazos<br/>                              |
| Doble<br/>              | Desplazarse hacia arriba<br/>                           | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble abajo<br/>            | Desplazarse hacia abajo<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble izquierda<br/>            | Desplazar a la izquierda<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble derecha<br/>           | Desplazar a la derecha<br/>                        | Fijo<br/>                | Punto de partida<br/>                                           |
| Triples<br/>              | Re Pág<br/>                             | Fijo<br/>                | Punto de partida<br/>                                           |
| Triple abajo<br/>            | Av Pág<br/>                           | Fijo<br/>                | Punto de partida<br/>                                           |
| Triple izquierda<br/>            | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Triple derecha<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Entre corchetes<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Entre corchetes<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Corchete-izquierda<br/>           | Inicio de la selección<br/>                  | Fijo<br/>                | Midpoint<br/>                                                 |
| Corchete-Right<br/>          | Fin de la selección<br/>                    | Fijo<br/>                | Midpoint<br/>                                                 |
| Llave<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Llave en minúsculas<br/>            | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Llave-izquierda<br/>             | Inicio de la selección descontinuada<br/>    | Fijo<br/>                | Midpoint<br/>                                                 |
| Llave-derecha<br/>            | Fin de la selección descontinuada<br/>      | Fijo<br/>                | Midpoint<br/>                                                 |
| Triple puntere<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | El punto de partida distingue el punto de acceso frecuente<br/>               |
| Puntear cuádruplemente<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | El punto de partida distingue el punto de acceso frecuente<br/>               |



 

 

 




