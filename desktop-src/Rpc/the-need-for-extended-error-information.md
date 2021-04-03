---
title: La necesidad de información de error extendida
description: Una dificultad principal asociada a la solución de problemas de RPC es la asignación de un código de error RPC al problema subyacente.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075460"
---
# <a name="the-need-for-extended-error-information"></a>La necesidad de información de error extendida

Una dificultad principal asociada a la solución de problemas de RPC es la asignación de un código de error RPC al problema subyacente. Un error de configuración o un problema de red puede dar lugar A que una o más estaciones de trabajo reciban errores de RPC \_ \_ \* , pero esa estación de trabajo solo puede mostrar el error, parafraseando o guardarlo en algún archivo de registro. Sea cual sea el método que se use, la persona que solucione el problema no tiene información esencial:

-   Dónde se produjo el error. Es posible que se haya producido en el equipo local, en un equipo remoto llamado por el equipo local o en un equipo remoto llamado por otro equipo remoto.
-   El código de error original que causó el problema. Para ajustarse al estándar de OSF, MS RPC asigna códigos de error a los códigos de RPC \_ S \_ \* . Sin embargo, los códigos de RPC \_ S \_ \* son demasiado genéricos y ofrecen poca información útil para la solución de problemas.
-   Cualquier información de contexto relacionada con la aparición del problema. Con errores que no son de RPC, los depuradores pueden detener el proceso y examinar el contexto en el que se produjo el error. Los errores de RPC suelen ser generados por un equipo o proceso remoto, que continúa el procesamiento después de devolver el error y sobrescribe cualquier contexto relacionado con el error.

 

 




