---
description: A continuación se muestra una lista de glifos de gestos que Microsoft planea admitir en el futuro como parte del reconocedor de gestos de Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifos sin implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361004"
---
# <a name="unimplemented-glyphs"></a>Glifos sin implementar

A continuación se muestra una lista de glifos de gestos que Microsoft planea admitir en el futuro como parte del reconocedor *de gestos de Microsoft*. Se está trabajando para garantizar que la precisión del reconocimiento de estos glifos sea alta (para evitar la activación accidental) y que se asignen a las operaciones adecuadas.

Para garantizar la *coherencia de los gestos usados* para *acciones comunes* entre aplicaciones, debe cumplir las siguientes sugerencias:

-   La *acción* es el comportamiento semántico sugerido asociado al gesto.
-   Para los gestos etiquetados como *Corregidos* en la tabla siguiente, se recomienda no cambiar el comportamiento semántico sugerido. Si una aplicación no necesita el comportamiento semántico especificado, se recomienda no volver a usar el gesto para otra acción o semántica.
-   No dude en asociar los comportamientos semánticos pertinentes a todos los demás gestos. Estos gestos se etiquetan como *específicos de la aplicación.* Para los gestos que tienen un comportamiento semántico sugerido, se recomienda usar el gesto para la semántica sugerida si la funcionalidad correspondiente existe en la aplicación.
-   El punto de acceso de un gesto es un punto distintivo en la geometría del gesto. El punto de acceso se puede usar para determinar dónde se realizó el gesto. La API de gestos permite determinar el punto de acceso para un gesto determinado. Sin embargo, no todos los gestos tienen un punto de referencia distintivo específico. Para aquellos que no tienen un punto de acceso rápido distintivo específico, el punto inicial se notifica como punto de acceso rápido.

> [!Note]  
> Algunos de los gestos tienen un punto de acceso que resulta ser el punto de partida distintivo. Se distinguen en la tabla.

 



| Nombre del gesto                      | Acción                                         | Fijo                           | Punto de acceso de acceso                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinito<br/>               | Cambiar al modo de gesto y salir de este<br/> | Fijo<br/>                | Punto de partida<br/>                                           |
| Cross<br/>                  | Eliminar<br/>                              | Específico de la aplicación<br/> | Intersección de los trazos<br/>                              |
| Marca de párrafo<br/>         | Nuevo párrafo<br/>                       | Fijo<br/>                | Punto de partida<br/>                                           |
| Sección<br/>                | Nueva sección<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Bala<br/>                 | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Viñeta cruzada<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Garabato<br/>               | Negrita<br/>                                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Swap<br/>                   | Exchange contenido<br/>                    | Específico de la aplicación<br/> | Centro del trazo hacia arriba<br/>                                  |
| Apertura<br/>                 | Abrir espacio entre palabras<br/>         | Específico de la aplicación<br/> | Centro del trazo hacia abajo<br/>                                |
| Closeup<br/>                | Cerrar espacio adicional<br/>                | Específico de la aplicación<br/> | Centro del espacio vertical entre los dos paréntesis<br/> |
| Rectángulo<br/>              | Selecciona el contenido incluido.<br/>            | Fijo<br/>                | Punto de partida<br/>                                           |
| Pulsación en círculo<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Pulsar<br/>                                                      |
| Círculo circular<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo cruzado<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo de línea vertical<br/>   | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Círculo de línea horizontal<br/> | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Flecha doble hacia arriba<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha doble hacia abajo<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha doble a la izquierda<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha doble a la derecha<br/>     | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha arriba a la izquierda<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha arriba a la derecha<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha abajo a la izquierda<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha abajo a la derecha<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha izquierda hacia arriba<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                               |
| Flecha izquierda hacia abajo<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha derecha hacia arriba<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Flecha derecha hacia abajo<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Vértice de la punta de la flecha<br/>                                   |
| Diagonal a la izquierda<br/>        | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal a la derecha<br/>       | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal a la izquierda<br/>      | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Diagonal a la derecha<br/>     | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-A<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-B<br/>         | Negrita<br/>                                | Fijo<br/>                | Punto de partida<br/>                                           |
| Latin-Letter-C<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-D<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-E<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-F<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-G<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-H<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-I<br/>         | Cursiva<br/>                              | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-J<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-K<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-L<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-M<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-N<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-O<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-P<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-Q<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-R<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-S<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-T<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-U<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-V<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-W<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-X<br/>         | Cortar<br/>                                 | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-Y<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Latin-Letter-Z<br/>         | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 0<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 1<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 2<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 3<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Digit-4<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 5<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 6<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 7<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 8<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dígito 9<br/>                | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Signo de interrogación<br/>          | Ayuda<br/>                                | Fijo<br/>                | Centro a lo largo del alto de la curva<br/>                     |
| Agudo<br/>                  | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Dólar<br/>                 | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Asterisk<br/>               | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Center<br/>                                                   |
| Plus<br/>                   | Pegar<br/>                               | Fijo<br/>                | Intersección de los trazos<br/>                              |
| Doble up<br/>              | Desplazarse hacia arriba<br/>                           | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble bajada<br/>            | Desplazarse hacia abajo<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble izquierda<br/>            | Desplazarse a la izquierda<br/>                         | Fijo<br/>                | Punto de partida<br/>                                           |
| Doble derecha<br/>           | Desplazarse a la derecha<br/>                        | Fijo<br/>                | Punto de partida<br/>                                           |
| Triple arriba<br/>              | Re Pág<br/>                             | Fijo<br/>                | Punto de partida<br/>                                           |
| Triple bajada<br/>            | Página abajo<br/>                           | Fijo<br/>                | Punto de partida<br/>                                           |
| Triple izquierda<br/>            | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Triple derecha<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Punto de partida<br/>                                           |
| Entre corchetes<br/>           | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Entre corchetes<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Corchete a la izquierda<br/>           | Inicio de la selección<br/>                  | Fijo<br/>                | Midpoint<br/>                                                 |
| Corchete a la derecha<br/>          | Final de la selección<br/>                    | Fijo<br/>                | Midpoint<br/>                                                 |
| Llaves<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Llave debajo<br/>            | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | Midpoint<br/>                                                 |
| Llave a la izquierda<br/>             | Inicio de la selección discontinua<br/>    | Fijo<br/>                | Midpoint<br/>                                                 |
| Llave derecha<br/>            | Fin de la selección discontinua<br/>      | Fijo<br/>                | Midpoint<br/>                                                 |
| Triple pulsación<br/>             | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | El punto inicial distingue el punto de acceso<br/>               |
| Pulsación con forma de condón<br/>          | Específico de la aplicación<br/>                | Específico de la aplicación<br/> | El punto inicial distingue el punto de acceso<br/>               |



 

 

 




