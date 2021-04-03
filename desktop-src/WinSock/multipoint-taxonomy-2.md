---
description: La taxonomía descrita en esta sección primero distingue el plano de control que se relaciona con la forma en que se establece una sesión Multipoint, desde el plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Taxonomía de Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907945"
---
# <a name="multipoint-taxonomy"></a>Taxonomía de Multipoint

La taxonomía descrita en esta sección primero distingue el plano de control que se relaciona con la forma en que se establece una sesión Multipoint, desde el plano de datos que se ocupa de la transferencia de datos entre los participantes de la sesión.

## <a name="session-establishment-in-the-control-plane"></a>Establecimiento de la sesión en el plano de control

En el plano de control hay dos tipos distintos de establecimiento de sesión:

-   raíz
-   no raíz

En el caso del control con raíz, existe un participante especial, la \_ raíz de c, que es diferente del resto de los miembros de esta sesión Multipoint, cada uno de los cuales se denomina \_ hoja c. La \_ raíz de c debe permanecer presente durante todo el tiempo de la sesión de Multipoint, ya que la sesión se divide en ausencia de la raíz de c \_ . La raíz de c \_ normalmente inicia la sesión de Multipoint mediante la configuración de la conexión a una \_ hoja de c o un número de hojas de c \_ . La raíz de c \_ puede agregar más \_ hojas de c o, en algunos casos, una \_ hoja c puede unir la raíz de c \_ en un momento posterior. Los ejemplos del plano de control con raíz se pueden encontrar en ATM y ST-II.

En el caso de un plano de control no raíz, todos los miembros que pertenecen a una sesión de Multipoint son, es decir, no existe ningún participante especial que actúe como raíz de c \_ . Cada \_ hoja de c debe agregarse a una sesión de Multipoint existente que siempre esté disponible (como en el caso de una dirección IP de multidifusión) o se haya configurado a través de algún mecanismo fuera de banda (OOB) que esté fuera del ámbito de la especificación de Windows Sockets.

Otra forma de ver esto es que una \_ raíz de c todavía existe, pero se puede considerar que está en la nube de red en lugar de uno de los participantes. Dado que una raíz de control sigue existiendo, también se podría considerar que un plano de control no raíz se ha modificado de forma implícita. Ejemplos de este tipo de esquemas de multipoint con raíz implícita:

-   Un puente de teleconferencia.
-   Sistema de multidifusión IP.
-   Una unidad de control Multipoint (MCU) en una videoconferencia H. 320.

## <a name="data-transfer-in-the-data-plane"></a>Transferencia de datos en el plano de datos

En el plano de datos, hay dos tipos de estilos de transferencia de datos:

-   raíz
-   no raíz

En un plano de datos raíz, existe un participante especial denominado \_ raíz d. La transferencia de datos solo se produce entre la \_ raíz d y el resto de los miembros de esta sesión Multipoint, cada una de las cuales se conoce como \_ hoja d. El tráfico puede ser unidireccional o bidireccional. Los datos que se envían desde la \_ raíz d están duplicados (si es necesario) y se entregan a cada \_ hoja d, mientras que los datos de las \_ hojas d solo van a la \_ raíz d. En el caso de un plano de datos con raíz, no se permite ningún tráfico entre las \_ hojas d. Un ejemplo de un protocolo cuya raíz se encuentra en el plano de datos es ST-II.

En un plano de datos no raíz, todos los participantes son iguales, es decir, todos los datos que envían se entregan a los demás participantes en la misma sesión de multipoint. Del mismo modo \_ , cada nodo de hoja d puede recibir datos de todas las demás \_ hojas d y, en algunos casos, de otros nodos que no participan en la sesión de multipoint. No existe ningún \_ nodo raíz d especial. IP: la multidifusión no tiene raíz en el plano de datos.

Tenga en cuenta que la pregunta de dónde se produce la duplicación de la unidad de datos o si un solo árbol compartido o varios árboles de ruta de acceso más corta se usan para la distribución Multipoint son problemas de protocolo y irrelevantes para la interfaz que la aplicación usaría para realizar comunicaciones multipunto. Por lo tanto, estos problemas no se tratan en este apéndice ni en la interfaz de Windows Sockets.

En la tabla siguiente se describe la taxonomía descrita anteriormente y se indica cómo se ajustan los esquemas existentes en cada una de las categorías. Tenga en cuenta que no parece haber ningún esquema existente que emplee un plano de control no raíz junto con un plano de datos raíz.

|                      | Plano de control con raíz | Plano de control no raíz (con raíz implícita) |
|----------------------|----------------------|-------------------------------------------|
| Plano de datos con raíz    | ATM, ST-II           | No hay ejemplos conocidos.                        |
| Plano de datos no raíz | T. 120                | IP-multidifusión, H. 320 (MCU)                 |



 

 

 



