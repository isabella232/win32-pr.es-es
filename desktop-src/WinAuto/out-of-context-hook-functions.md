---
title: Funciones de enlace fuera de contexto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Más información sobre: funciones de enlace fuera de contexto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911773"
---
# <a name="out-of-context-hook-functions"></a>Funciones de enlace fuera de contexto

En la siguiente lista se describen los aspectos clave de las funciones de enlace fuera de contexto:

-   Las funciones de enlace fuera del contexto se encuentran en el espacio de direcciones del cliente, tanto si están en el cuerpo del código como en un archivo DLL.
-   Las funciones de enlace fuera de contexto no se asignan al espacio de direcciones del servidor.
-   Cuando se desencadena un evento, se calculan las referencias de los parámetros de la función de enlace a través de los límites del proceso.
-   Las funciones de enlace fuera de contexto son notablemente más lentas que las funciones de enlace en contexto debido al cálculo de referencias.
-   El sistema pone en cola las notificaciones de eventos para que lleguen de forma asincrónica (debido al tiempo necesario para realizar el cálculo de referencias).

Aunque las notificaciones de eventos son asincrónicas, Microsoft Active Accessibility garantiza que la función de devolución de llamada recibe todos los eventos en el orden en el que se generan.

El componente de usuario del sistema operativo asigna memoria a los eventos que se controlan mediante funciones de enlace fuera de contexto. La memoria se libera cuando las funciones de enlace devuelven. Si una función de enlace no procesa los eventos lo suficientemente rápido, los recursos de usuario se reducen, lo que finalmente produce un error o un tiempo de respuesta muy lento. Estos problemas pueden producirse si:

-   Los eventos se desencadenan muy rápidamente.
-   El sistema es lento.
-   La función de enlace procesa los eventos lentamente.
-   El cliente se ejecuta en Windows 9x.

 

 




