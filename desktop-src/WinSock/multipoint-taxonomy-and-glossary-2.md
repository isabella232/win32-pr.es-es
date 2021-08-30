---
description: La taxonomía que se describe a continuación distingue primero el plano de control que se preocupa por la forma en que se establece una sesión multipunto, del plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Taxonomía y glosario multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5b42690ccd6d4037452d9f4071d9f28d9e2ca9ee5a6ebbd3beca0bc222a7a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097705"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Taxonomía y glosario multipunto

La taxonomía que se describe a continuación distingue primero el plano de control que se preocupa por la forma en que se establece una sesión multipunto, del plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.

En el plano de control, hay dos tipos distintos de establecimiento de sesión:

-   Arraigada
-   nonrooted

Para un plano de control raíz, existe un participante especial, denominado raíz c, que es diferente del resto de los miembros de esta sesión multipunto, cada uno de los cuales se denomina hoja \_ \_ c. La raíz de c debe permanecer presente durante todo el período de la sesión multipunto, ya que la sesión se dividirá en ausencia \_ de la raíz de \_ c. Normalmente, la raíz de c inicia la sesión de varios puntos configurando la conexión a una hoja \_ c o a varias hojas de \_ \_ c. La raíz de c puede agregar más hojas de c o, en algunos casos, una hoja c puede unirse a la raíz \_ \_ de c más \_ \_ adelante. Puede encontrar ejemplos del plano de control raíz en ATM y ST-II.

En el caso de un plano de control no raíz, todos los miembros que pertenecen a una sesión de varios puntos son hojas, es decir, no existe ningún participante especial que actúe como raíz de \_ c. Cada hoja de c debe agregarse a una sesión multipunto existente que esté siempre disponible (como en el caso de una dirección de multidifusión IP) o que se haya configurado a través de algún mecanismo de OOB que esté fuera del ámbito de esta discusión (y, por tanto, no se haya abordado en las extensiones de sockets de \_ Windows propuestas). Otra manera de ver esto es que todavía existe una raíz de C, pero se puede considerar que está en la nube de red en lugar de uno \_ de los participantes. Dado que todavía existe una raíz de control, también se podría considerar que un plano de control no raíz está enraizado implícitamente. Algunos ejemplos de este tipo de esquemas multipunto con raíz implícita son: un puente de teleconferencia, el sistema de multidifusión IP, una unidad de control multipunto (MCU) en una conferencia de vídeo H.320, etc.

En el plano de datos, también hay dos tipos de estilos de transferencia de datos:

-   Arraigada
-   nonrooted

En un plano de datos con raíz, existe un participante especial denominado raíz \_ d. La transferencia de datos solo se produce entre la raíz d y el resto de los miembros de esta sesión multipunto, cada uno de los cuales se conoce \_ como hoja \_ d. El tráfico podría ser unidireccional o bidireccional. Los datos enviados desde la raíz d se duplicarán (si es necesario) y se entregarán a cada hoja d, mientras que los datos de las hojas d solo irán a la \_ \_ raíz \_ \_ d. En el caso de un plano de datos raíz, no se permite tráfico entre hojas \_ d. Un ejemplo de un protocolo que usa un plano de datos con raíz es ST-II.

En un plano de datos no raíz, todos los participantes son iguales en el sentido de que los datos que envíen se entregarán a todos los demás participantes en la misma sesión multipunto. Del mismo modo, cada nodo hoja d podrá recibir datos de todas las demás hojas d y, en algunos casos, de otros nodos que no participan también en la sesión \_ \_ multipunto. No existe ningún \_ nodo raíz especial. La multidifusión IP es un ejemplo de un protocolo que usa un plano de datos no raíz.

Tenga en cuenta que la pregunta de dónde se produce la duplicación de unidades de datos o si se usa un único árbol compartido o varios árboles de ruta de acceso más cortas para la distribución de varios puntos son problemas de protocolo. Por lo tanto, son irrelevantes para la interfaz que el cliente usaría para realizar comunicaciones multipunto. Por lo tanto, la interfaz Windows Sockets no aborda estos problemas.

En la tabla siguiente se muestra la taxonomía descrita anteriormente e indica cómo encajan los esquemas existentes en cada una de las categorías de plano de datos y control. Tenga en cuenta que no parece haber ningún esquema multipunto que emplee un plano de control no raíz junto con un plano de datos raíz.

| Plano de datos           | Ejemplos de plano de control con raíz | Ejemplos de plano de control no raíz (raíz implícita) |
|----------------------|-------------------------------|----------------------------------------------------|
| Plano de datos con raíz    | ATM, ST-II                    | No hay ejemplos conocidos                                  |
| Plano de datos no raíz | T.120                         | Multidifusión IP, H.320 (MCU)                          |



 

 

 



