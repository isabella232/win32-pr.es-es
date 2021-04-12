---
title: In-Context funciones de enlace
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Más información sobre: In-Context funciones de enlace'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279299"
---
# <a name="in-context-hook-functions"></a>In-Context funciones de enlace

En la siguiente lista se describen los aspectos clave de las funciones de enlace en contexto:

-   Las funciones de enlaces en contexto deben estar ubicadas en una biblioteca de vínculos dinámicos (DLL) que el sistema asigna al espacio de direcciones del servidor.
-   Las funciones de enlace en contexto comparten el espacio de direcciones con el servidor.
-   Cuando el servidor desencadena un evento, el sistema llama a una función de enlace sin serialización (empaquetado y envío de parámetros de interfaz a través de los límites del proceso).
-   Las funciones de enlace en contexto suelen ser muy rápidas y reciben notificaciones de eventos sincrónicamente porque no hay ningún cálculo de referencias.
-   Es posible que algunos eventos se entreguen fuera de proceso, aunque solicite que se entreguen en proceso (mediante la \_ marca de INCONTEXTO WINEVENT). Podría ver esta situación con problemas de interoperabilidad de aplicaciones de 64 y 32 bits y con eventos de la consola de Windows.

 

 




