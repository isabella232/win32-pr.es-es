---
title: Infraestructura de WinEvents
description: El sistema operativo Windows Microsoft incluye una característica, denominada WinEvents, que permite a los procesos y aplicaciones que se ejecutan en el escritorio de Windows intercambiar determinados tipos de información.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8662cdcbfa9546ce04dc787e7089f68ba1c03137c41067c20792f7da111cf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563290"
---
# <a name="winevents"></a>WinEvents

El sistema operativo Windows Microsoft incluye una característica, denominada *WinEvents,* que permite a los procesos y aplicaciones que se ejecutan en el escritorio Windows intercambiar determinados tipos de información. Las herramientas de accesibilidad que usan Microsoft Automatización de la interfaz de usuario y Microsoft Active Accessibility están entre los usuarios principales de WinEvents.

En el contexto de accesibilidad, los proveedores de Automatización de la interfaz de usuario y los servidores Microsoft Active Accessibility usan WinEvents para notificar a los clientes los cambios en una interfaz de usuario de la aplicación, como cuando se ha creado o destruyedo un elemento de interfaz de usuario, o cuando ha cambiado un nombre, estado o valor de elemento.

En esta sección se proporcionan sugerencias, directrices y ejemplos para ayudar a los clientes a controlar WinEvents y a ayudar a los servidores a determinar cuándo desencadenar el WinEvent adecuado.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué son los winevents?](what-are-winevents.md)
-   [Registrar una función de enlace](registering-a-hook-function.md)
-   [Eventos de nivel de sistema Object-Level datos](system-level-and-object-level-events.md)
-   [Funciones de enlace en contexto y fuera de contexto](in-context-and-out-of-context-hook-functions.md)
-   [Protección contra la reenlazancia en las funciones de enlace](guarding-against-reentrancy-in-hook-functions.md)
-   [Asignación de los IDs de WinEvent](allocation-of-winevent-ids.md)

Para obtener información general sobre el proceso de notificación de eventos Microsoft Active Accessibility, consulte [WinEvents](winevents-overview.md) en [Technical Overview](technical-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura común](common-infrastructure.md)
</dt> </dl>

 

 




