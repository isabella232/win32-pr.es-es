---
title: In-Context de enlace
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Más información sobre: In-Context de enlace de datos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbeb6340642d63700901d9306aea5dca20b26ce46790d900e26e42875571379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565566"
---
# <a name="in-context-hook-functions"></a>In-Context de enlace

En la lista siguiente se describen los aspectos clave de las funciones de enlace en contexto:

-   Las funciones de enlaces en contexto deben encontrarse en una biblioteca de vínculos dinámicos (DLL) que el sistema asigna al espacio de direcciones del servidor.
-   Las funciones de enlace en contexto comparten el espacio de direcciones con el servidor.
-   Cuando el servidor desencadena un evento, el sistema llama a una función de enlace sin serializar (empaquetar y enviar parámetros de interfaz a través de los límites del proceso).
-   Las funciones de enlace en contexto tienden a ser muy rápidas y reciben notificaciones de eventos sincrónicamente porque no hay serialización.
-   Algunos eventos se pueden entregar fuera de proceso, aunque solicite que se entreguen en proceso (mediante la marca \_ WINEVENT INCONTEXT). Es posible que vea esta situación con problemas de interoperabilidad de aplicaciones de 64 y 32 bits y con Windows eventos de consola.

 

 




