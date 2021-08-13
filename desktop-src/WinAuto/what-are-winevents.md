---
title: ¿Qué son los winevents?
description: Las aplicaciones de servidor y el sistema operativo usan WinEvents para notificar a los clientes cuando se produce un cambio en el sistema o en la interfaz de usuario.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c177183fa776a6becf52d62b86fe0ae6785c5be19dd287324ba3345b586af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563516"
---
# <a name="what-are-winevents"></a>¿Qué son los winevents?

Las aplicaciones de servidor y el sistema operativo usan WinEvents para notificar a los clientes cuando se produce un cambio en el sistema o en la interfaz de usuario.

La compatibilidad con WinEvent es una característica del Windows operativo que proporciona:

-   Una manera sencilla de que los clientes se registren para las notificaciones de eventos.
-   Mecanismo para insertar código de cliente en servidores.
-   Enrutamiento de eventos de servidores a clientes interesados.
-   Generación automática de eventos para la mayoría de los controles basados en **HWND.**

La generación de **eventos para controles basados** en HWND es especialmente importante para los desarrolladores de servidores. El Microsoft Active Accessibility en tiempo de ejecución proporciona servidores proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos los elementos de la interfaz de usuario estándar. De forma similar, el sistema genera automáticamente los WinEvents adecuados cada vez que crea, destruye, mueve, cambia el tamaño o realiza cualquier otra acción en un control basado en **HWND.**

El sistema admite automáticamente algunos eventos WinEvent, incluidos **los eventos HWND** generales. Otros tipos de WinEvents, como cambios de estado o eventos de selección específicos de un control determinado, son compatibles con Microsoft Active Accessibility servidores.

Cuando se produce un evento que afecta a la interfaz de usuario, los servidores pueden difundir una notificación de eventos a todos los clientes interesados llamando a [**la función NotifyWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) La llamada de función incluye información que identifica el tipo de evento que se produjo y el elemento de interfaz de usuario al que se aplica el evento. Los clientes pueden usar esta información para recuperar un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario y recopilar más información.

Por ejemplo, para notificar a los clientes que el nombre de un control ha cambiado, un servidor llama a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) y pasa [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) en el parámetro de evento. El sistema responde determinando qué clientes se han registrado para recibir ese evento concreto y llama a su función de devolución de llamada registrada. Si ningún cliente se ha registrado para el evento, la llamada del servidor a **NotifyWinEvent** es comparable a una "sin operación" y el impacto en el rendimiento es insignificante.

Los servidores [**llaman a NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para anunciar el evento al sistema después de que se haya producido el evento. Nunca deben notificar al sistema un evento antes de que se produzca el evento.

Para recibir notificaciones de eventos, los clientes registran funciones de enlace de devolución de llamada mediante [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Los clientes establecen una función de enlace única para todos los eventos posibles o varias funciones de enlace para intervalos discretos de eventos. Para obtener más información, [vea Registrar una función de enlace](registering-a-hook-function.md).

Cuando Microsoft Active Accessibility notificación de un evento, llama a cualquier función de enlace registrada para ese evento, pasando los parámetros de [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




