---
title: Infraestructura de WinEvents
description: El sistema operativo Microsoft Windows incluye una característica, denominada WinEvents, que permite a los procesos y aplicaciones que se ejecutan en el escritorio de Windows intercambiar determinados tipos de información.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785554"
---
# <a name="winevents"></a>WinEvents

El sistema operativo Microsoft Windows incluye una característica, denominada *WinEvents*, que permite a los procesos y aplicaciones que se ejecutan en el escritorio de Windows intercambiar determinados tipos de información. Las herramientas de accesibilidad que usan la automatización de la interfaz de usuario de Microsoft y Microsoft Active Accessibility se encuentran entre los usuarios principales de WinEvents.

En el contexto de accesibilidad, los proveedores de automatización de la interfaz de usuario y los servidores de Microsoft Active Accessibility utilizan WinEvents para notificar a los clientes de los cambios en una interfaz de usuario de la aplicación, como cuando se ha creado o destruido un elemento de la interfaz de usuario, o cuando ha cambiado el nombre, el estado o el valor de un elemento.

En esta sección se proporcionan sugerencias, instrucciones y ejemplos para ayudar a los clientes a controlar WinEvents y ayudar a los servidores a determinar cuándo se debe desencadenar el WinEvent adecuado.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué son los WinEvents?](what-are-winevents.md)
-   [Registro de una función de enlace](registering-a-hook-function.md)
-   [Eventos de Object-Level y de nivel de sistema](system-level-and-object-level-events.md)
-   [Funciones de enlace en contexto y fuera de contexto](in-context-and-out-of-context-hook-functions.md)
-   [Protección contra reentrada en funciones de enlace](guarding-against-reentrancy-in-hook-functions.md)
-   [Asignación de identificadores de WinEvent](allocation-of-winevent-ids.md)

Para obtener información general sobre el proceso de notificación de eventos en Microsoft Active Accessibility, consulte [WinEvents](winevents-overview.md) en [Technical Overview (introducción técnica](technical-overview.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura común](common-infrastructure.md)
</dt> </dl>

 

 




