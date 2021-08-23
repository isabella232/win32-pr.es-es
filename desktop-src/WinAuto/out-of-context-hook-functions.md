---
title: Funciones de enlace fuera de contexto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Más información sobre: Funciones de enlace fuera de contexto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e41e9a6bba1f705c3c5dc8781b2663be22086955f5dee45f07022504d0ccbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133748"
---
# <a name="out-of-context-hook-functions"></a>Funciones de enlace fuera de contexto

En la lista siguiente se describen los aspectos clave de las funciones de enlace fuera de contexto:

-   Las funciones de enlace fuera de contexto se encuentran en el espacio de direcciones del cliente, ya sea en el cuerpo del código o en un archivo DLL.
-   Las funciones de enlace fuera de contexto no se asignan al espacio de direcciones del servidor.
-   Cuando se desencadena un evento, los parámetros de la función de enlace se serializan a través de los límites del proceso.
-   Las funciones de enlace fuera de contexto son notablemente más lentas que las funciones de enlace en contexto debido a la serialización.
-   El sistema pone en cola las notificaciones de eventos para que lleguen de forma asincrónica (debido al tiempo necesario para realizar la serialización).

Aunque las notificaciones de eventos son asincrónicas, Microsoft Active Accessibility garantiza que la función de devolución de llamada recibe todos los eventos en el orden en que se generan.

El componente USER del sistema operativo asigna memoria para los eventos que se controlan mediante funciones de enlace fuera de contexto. La memoria se libera cuando se devuelven las funciones de enlace. Si una función de enlace no procesa los eventos lo suficientemente rápido, los recursos USER se reducen, lo que finalmente produce un error o tiempos de respuesta extremadamente lentos. Estos problemas pueden producirse si:

-   Los eventos se desencadenan muy rápidamente.
-   El sistema es lento.
-   La función de enlace procesa los eventos lentamente.
-   El cliente se ejecuta en Windows 9x.

 

 




