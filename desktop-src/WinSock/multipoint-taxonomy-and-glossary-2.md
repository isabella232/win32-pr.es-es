---
description: La taxonomía que se describe a continuación distingue primero el plano de control que se relaciona con la forma en que se establece una sesión Multipoint, desde el plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Taxonomía y Glosario de Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ecdfe59640ec58b592aace4e46c66faf752281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677368"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Taxonomía y Glosario de Multipoint

La taxonomía que se describe a continuación distingue primero el plano de control que se relaciona con la forma en que se establece una sesión Multipoint, desde el plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.

En el plano de control, hay dos tipos distintos de establecimiento de sesión:

-   raíz
-   no raíz

En el caso de un plano de control con raíz, existe un participante especial, denominado raíz de c \_ , que es diferente al resto de los miembros de esta sesión Multipoint, cada uno de los cuales se denomina \_ hoja c. La \_ raíz de c debe permanecer presente durante todo el tiempo de la sesión de Multipoint, ya que la sesión se dividirá en ausencia de la raíz de c \_ . La raíz de c \_ normalmente inicia la sesión de Multipoint mediante la configuración de la conexión a una \_ hoja de c o un número de hojas de c \_ . La raíz de c \_ puede agregar más \_ hojas de c o, en algunos casos, una \_ hoja c puede unir la raíz de c \_ en un momento posterior. Los ejemplos del plano de control con raíz se pueden encontrar en ATM y ST-II.

En el caso de un plano de control no raíz, todos los miembros que pertenecen a una sesión de Multipoint se salen, es decir, no existe ningún participante especial que actúe como raíz de c \_ . Cada \_ hoja de c tiene que agregarse a una sesión de Multipoint existente previamente que siempre está disponible (como en el caso de una dirección IP de multidifusión) o que se ha configurado a través de algún mecanismo de OOB que está fuera del ámbito de este debate (y, por lo tanto, no se trata en las extensiones de Windows Sockets propuestas). Otra forma de ver esto es que una \_ raíz de c todavía existe, pero se puede considerar que está en la nube de red en lugar de uno de los participantes. Dado que una raíz de control sigue existiendo, también se podría considerar que un plano de control no raíz se ha modificado de forma implícita. Algunos ejemplos de este tipo de esquemas de multipoint con raíz implícita son: un puente de teleconferencia, el sistema de multidifusión IP, una unidad de control Multipoint (MCU) en una videoconferencia H. 320, etc.

En el plano de datos, también hay dos tipos de estilos de transferencia de datos:

-   raíz
-   no raíz

En un plano de datos raíz, existe un participante especial denominado \_ raíz d. La transferencia de datos solo se produce entre la \_ raíz d y el resto de los miembros de esta sesión Multipoint, cada una de las cuales se conoce como \_ hoja d. El tráfico puede ser unidireccional o bidireccional. Los datos que se envíen desde la raíz d se \_ duplicarán (si es necesario) y se entregarán a cada \_ hoja d, mientras que los datos de las \_ hojas d solo Irán a la \_ raíz d. En el caso de un plano de datos con raíz, no se permite el tráfico entre las \_ hojas d. Un ejemplo de un protocolo que utiliza un plano de datos raíz es ST-II.

En un plano de datos no raíz, todos los participantes son iguales en el sentido de que los datos que envían se entregarán a los demás participantes en la misma sesión de multipoint. Del mismo modo, cada \_ nodo hoja d podrá recibir los datos de todas las demás \_ hojas d y, en algunos casos, de otros nodos que no participen también en la sesión de multipoint. No existe ningún \_ nodo raíz d especial. IP-multidifusión es un ejemplo de un protocolo que utiliza un plano de datos no raíz.

Tenga en cuenta que la pregunta de dónde se produce la duplicación de la unidad de datos o si se usa un solo árbol compartido o varios árboles de ruta de acceso más corta para la distribución Multipoint son problemas de protocolo. Como tal, son irrelevantes para la interfaz que el cliente usaría para realizar comunicaciones multipunto. Por lo tanto, estos problemas no se solucionan mediante la interfaz de Windows Sockets.

En la tabla siguiente se describe la taxonomía descrita anteriormente y se indica cómo se ajustan los esquemas existentes en cada una de las categorías de control y plano de datos. Tenga en cuenta que no parece haber ningún esquema Multipoint que emplee un plano de control no raíz junto con un plano de datos raíz.

| Plano de datos           | Ejemplos de plano de control con raíz | Ejemplos de plano de control no raíz (con raíz implícita) |
|----------------------|-------------------------------|----------------------------------------------------|
| Plano de datos con raíz    | ATM, ST-II                    | No hay ejemplos conocidos                                  |
| Plano de datos no raíz | T. 120                         | IP-multidifusión, H. 320 (MCU)                          |



 

 

 



