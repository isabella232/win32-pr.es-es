---
description: La taxonomía descrita en esta sección distingue primero el plano de control que se ocupa de la forma en que se establece una sesión de varios puntos, del plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Taxonomía multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1928dde2935ab803d95d73db225f7b3be0bc051a082d3bdae937e9b8e7da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097725"
---
# <a name="multipoint-taxonomy"></a>Taxonomía multipunto

La taxonomía descrita en esta sección distingue primero el plano de control que se ocupa de la forma en que se establece una sesión de varios puntos, del plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.

## <a name="session-establishment-in-the-control-plane"></a>Establecimiento de sesión en el plano de control

En el plano de control hay dos tipos distintos de establecimiento de sesión:

-   Arraigada
-   no raíz

En el caso del control con raíz, existe un participante especial, raíz c, que es diferente del resto de los miembros de esta sesión de varios puntos, cada uno de los cuales se denomina \_ hoja \_ c. La raíz de c debe permanecer presente durante todo el tiempo que dure la sesión multipunto, ya que la sesión se divide en ausencia \_ de la raíz de \_ c. Normalmente, la raíz de c inicia la sesión de varios puntos configurando la conexión a una hoja \_ c o varias hojas de \_ \_ c. La raíz de c puede agregar más hojas de c o, en algunos casos, una hoja c puede unirse a la raíz \_ \_ de c más \_ \_ adelante. Puede encontrar ejemplos del plano de control con raíz en ATM y ST-II.

En el caso de un plano de control no raíz, todos los miembros que pertenecen a una sesión de varios puntos son hojas, es decir, no existe ningún participante especial que actúe como raíz \_ de C. Cada hoja c debe agregarse a una sesión multipunto preexistencia que esté siempre disponible (como en el caso de una dirección de multidifusión IP) o que se haya configurado a través de algún mecanismo fuera de banda (OOB) que esté fuera del ámbito de la especificación \_ de sockets de Windows.

Otra manera de ver esto es que todavía existe una raíz de C, pero se puede considerar que está en la nube de red en lugar de uno \_ de los participantes. Dado que todavía existe una raíz de control, también se podría considerar que un plano de control no raíz tiene raíz implícita. Algunos ejemplos de este tipo de esquemas multipunto con raíz implícita son:

-   Un puente de teleconferencia.
-   Sistema de multidifusión IP.
-   Una unidad de control multipunto (MCU) en una videoconferencia H.320.

## <a name="data-transfer-in-the-data-plane"></a>Transferencia de datos en el plano de datos

En el plano de datos, hay dos tipos de estilos de transferencia de datos:

-   Arraigada
-   no raíz

En un plano de datos con raíz, existe un participante especial denominado \_ raíz d. La transferencia de datos solo se produce entre la raíz d y el resto de los miembros de esta sesión multipunto, cada uno de los cuales se conoce \_ como hoja \_ d. El tráfico podría ser unidireccional o bidireccional. Los datos enviados desde la raíz d se duplican (si es necesario) y se entregan a cada hoja d, mientras que los datos de las hojas d solo van a la \_ \_ raíz \_ \_ d. En el caso de un plano de datos con raíz, no se permite tráfico entre hojas \_ d. Un ejemplo de un protocolo que se basa en el plano de datos es ST-II.

En un plano de datos no raíz, todos los participantes son iguales, es decir, los datos que envían se entregan a todos los demás participantes en la misma sesión multipunto. Del mismo modo, cada nodo hoja d puede recibir datos de todas las demás hojas d y, en algunos casos, de otros nodos que no participan en la \_ \_ sesión de varios puntos. No existe ningún \_ nodo raíz d especial. La multidifusión IP no se genera en el plano de datos.

Tenga en cuenta que la pregunta de dónde se produce la duplicación de unidades de datos o si se usa un árbol único compartido o varios árboles de ruta de acceso más cortas para la distribución de varios puntos son problemas de protocolo y son irrelevantes para la interfaz que la aplicación usaría para realizar comunicaciones multipunto. Por lo tanto, estos problemas no se abordan en este apéndice ni en la Windows sockets.

En la tabla siguiente se muestra la taxonomía descrita anteriormente e indica cómo encajan los esquemas existentes en cada una de las categorías. Tenga en cuenta que no parece haber ningún esquema existente que emplee un plano de control no raíz junto con un plano de datos con raíz.

|                      | Plano de control con raíz | Plano de control no raíz (raíz implícita) |
|----------------------|----------------------|-------------------------------------------|
| Plano de datos con raíz    | ATM, ST-II           | No hay ejemplos conocidos.                        |
| Plano de datos no raíz | T.120                | Multidifusión IP, H.320 (MCU)                 |



 

 

 



