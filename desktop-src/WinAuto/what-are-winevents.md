---
title: Qué son WinEvents
description: Las aplicaciones de servidor y el sistema operativo usan WinEvents para notificar a los clientes cuando se produce un cambio en el sistema o en la interfaz de usuario.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704771"
---
# <a name="what-are-winevents"></a>¿Qué son los WinEvents?

Las aplicaciones de servidor y el sistema operativo usan WinEvents para notificar a los clientes cuando se produce un cambio en el sistema o en la interfaz de usuario.

La compatibilidad con WinEvent es una característica del sistema operativo Windows que proporciona:

-   Una manera sencilla de que los clientes se registren para las notificaciones de eventos.
-   Mecanismo para insertar código de cliente en servidores.
-   Enrutamiento de eventos de servidores a clientes interesados.
-   Generación automática de eventos para la mayoría de los controles basados en **hWnd**.

La generación de eventos para los controles basados en **hWnd** es especialmente importante para los desarrolladores de servidor. El tiempo de ejecución de Microsoft Active Accessibility proporciona proxies [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos los elementos de la interfaz de usuario estándar. Del mismo modo, el sistema genera automáticamente el WinEvents adecuado cada vez que crea, destruye, mueve, cambia de tamaño o realiza cualquier otra acción en un control basado en **hWnd**.

El sistema admite automáticamente algunos WinEvents, incluidos los eventos de **hWnd** generales. Otros tipos de WinEvents, como los cambios de estado o los eventos de selección específicos de un control determinado, son compatibles con los servidores de Microsoft Active Accessibility.

Cuando se produce un evento que afecta a la interfaz de usuario, los servidores pueden difundir una notificación de eventos a todos los clientes interesados llamando a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) . La llamada de función incluye información que identifica el tipo de evento que se ha producido y el elemento de la interfaz de usuario al que se aplica el evento. Los clientes pueden usar esta información para recuperar un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de la interfaz de usuario y recopilar más información.

Por ejemplo, para notificar a los clientes que ha cambiado el nombre de un control, un servidor llama a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) y pasa el [**objeto de evento \_ \_ NameChange (**](event-constants.md) en el parámetro de evento. El sistema responde determinando qué clientes se han registrado para recibir ese evento concreto y llama a su función de devolución de llamada registrada. Si no se ha registrado ningún cliente para el evento, la llamada del servidor a **NotifyWinEvent** es comparable a una "sin operación" y el impacto en el rendimiento es insignificante.

Los servidores llaman a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para anunciar el evento al sistema después de que se haya producido el evento. Nunca deben notificar al sistema de un evento antes de que se produzca el evento.

Para recibir notificaciones de eventos, los clientes registran funciones de enlace de devolución de llamada mediante [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Los clientes establecen una única función de enlace para todos los posibles eventos o varias funciones de enlace para intervalos de eventos discretos. Para obtener más información, vea [registrar una función de enlace](registering-a-hook-function.md).

Cuando Microsoft Active Accessibility recibe una notificación de un evento, llama a las funciones de enlace que se registraron para ese evento, pasando a lo largo de los parámetros de [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




