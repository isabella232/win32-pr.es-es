---
title: La necesidad de información de error extendida
description: Una dificultad principal asociada a la solución de problemas de RPC es asignar un código de error de RPC al problema subyacente.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce13e2cb30c7cd9f2db4d7f518eb0a747cd15b2ba1ff7962cf5f41fbc9cf552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016805"
---
# <a name="the-need-for-extended-error-information"></a>La necesidad de información de error extendida

Una dificultad principal asociada a la solución de problemas de RPC es asignar un código de error de RPC al problema subyacente. Un error de configuración o un problema de red puede dar lugar a que una o varias estaciones de trabajo reciban errores de RPC S, pero esa estación de trabajo solo puede mostrar el error, parafrasalizarlo o guardarlo en algún archivo de \_ \_ \* registro. Independientemente del enfoque que se utilice, la persona que solucione el problema carece de información esencial:

-   Donde se produjo el error. Puede que se haya producido en el equipo local, en un equipo remoto al que llama el equipo local o en un equipo remoto al que llama otro equipo remoto.
-   Código de error original que produjo el problema. Para cumplir con el estándar OSF, MS RPC asigna códigos de error a códigos RPC \_ \_ \* S. Sin embargo, los códigos RPC \_ S \_ \* son demasiado genéricos y ofrecen poca información útil para solucionar problemas.
-   Cualquier información de contexto relacionada con la aparición del problema. Con errores que no son RPC, los depuradores pueden detener el proceso y examinar el contexto en el que se produjo el error. A menudo, un proceso o equipo remoto genera errores RPC, que continúa el procesamiento después de devolver el error y sobrescribe cualquier contexto relacionado con el error.

 

 




