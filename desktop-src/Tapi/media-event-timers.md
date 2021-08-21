---
description: Muchas aplicaciones dependen de la relación de tiempo entre eventos multimedia (por ejemplo, dígitos DTMF recibidos) para determinar la naturaleza de una operación solicitada.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Temporizadores de eventos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6fc2d7b064eba81c07dcae8e48e12b2cbf2d68a6a7b11e3045f7570e0b7693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863124"
---
# <a name="media-event-timers"></a>Temporizadores de eventos multimedia

Muchas aplicaciones dependen de la relación de tiempo entre eventos multimedia (por ejemplo, dígitos DTMF recibidos) para determinar la naturaleza de una operación solicitada. Por ejemplo, en una aplicación de correo de voz, dos dígitos dtmf "1" consecutivos pueden significar "hacer una copia de seguridad de dos segmentos" o "reproducir desde el principio del mensaje", en función del tiempo transcurrido entre los dos dígitos. En un entorno de cliente/servidor, si la detección de DTMF se realiza en un procesador independiente del en el que se ejecuta la aplicación, la latencia en la red de área local hace que sea muy probable que la relación de tiempo entre los eventos multimedia se sesme, con el resultado de que estas diferencias basadas en el tiempo podrían perderse o volverse poco confiables.

Para resolver este problema, se puede crear una marca de tiempo de varios mensajes TAPI. Dado que es el tiempo relativo entre estos eventos lo importante, la "hora del reloj" del evento no es importante y el tiempo de subsegundos está implicado, estas marcas de tiempo usan la "hora desde el inicio de Windows" de resolución de milisegundos devuelta por la función [**GetTickCount.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) Las aplicaciones deben tener en cuenta que este es el número de pasos en el servidor (o la máquina en la que se ejecuta el proveedor de servicios que administra directamente el hardware) y no es necesariamente la misma máquina en la que se ejecuta la aplicación. Por lo tanto, las marcas de tiempo de estos mensajes TAPI solo se pueden comparar entre sí y no con el valor devuelto por **GetTickCount** en el procesador en el que se ejecuta la aplicación.

Los mensajes TAPI con marca de tiempo son: [**LINE \_ GATHERDIGITS,**](line-gatherdigits.md) [**LINE \_ GENERATE,**](line-generate.md) [**LINE \_ MONITORDIGITS,**](line-monitordigits.md) [**LINE \_ MONITORMEDIA**](line-monitormedia.md)y [**LINE \_ MONITORTONE.**](line-monitortone.md) El recuento de pasos se inserta *en dwParam3* de estos mensajes. Si el proveedor de servicios no admite la marca de tiempo (lo que se indica mediante la configuración *dwParam3* del proveedor de servicios en estos mensajes en 0), el propio TAPI insertará el recuento de tics en *dwParam3* de todos estos mensajes (se puede sesgar un poco, pero menos que si la aplicación hubiera hecho lo mismo después de que los mensajes hubieran recorrido un esquema de comunicación entre procesos).

 

 
