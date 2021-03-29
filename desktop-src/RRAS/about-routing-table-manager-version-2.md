---
title: Acerca del administrador de tablas de enrutamiento, versión 2
description: En la siguiente documentación se describe la tecnología del administrador de tablas de enrutamiento versión 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2, descrito
- Administrador de tabla de enrutamiento versión 2 RRAS
- Administrador de tablas de enrutamiento versión 2 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075844"
---
# <a name="about-routing-table-manager-version-2"></a>Acerca del administrador de tablas de enrutamiento, versión 2

En la siguiente documentación se describe la tecnología del administrador de tablas de enrutamiento versión 2 (RTMv2). RTMv2 API es una característica de Windows 2000 y sistemas operativos posteriores que puede usar para escribir protocolos de enrutamiento que interactúan con el administrador de tablas de enrutamiento.

El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).

RTMv2 no está disponible para la versión 4,0 de Windows NT. Además, RTMv2 no se puede usar para protocolos de enrutamiento IPX que se ejecutan en Windows NT 4,0 o Windows 2000. Si usa IPX o escribe protocolos de enrutamiento para Windows NT 4,0, consulte [acerca de la versión 1 del administrador de tablas de enrutamiento](about-routing-table-manager-version-1.md).

En esta información general se describen los temas siguientes:

-   [Componentes de la arquitectura del administrador de tablas de enrutamiento](components-of-the-routing-table-manager-architecture.md)
-   [Registro con el administrador de tablas de enrutamiento](registering-with-the-routing-table-manager.md)
-   [Enumerar entidades registradas](enumerating-registered-entities.md)
-   [Usar métodos](using-methods.md)
-   [Usar punteros opacos](using-opaque-pointers.md)
-   [Marcar rutas para el estado Hold-Down](marking-routes-for-the-hold-down-state.md)
-   [Agregar rutas](adding-routes.md)
-   [Recuperar información de ruta](retrieving-route-information.md)
-   [Actualizar rutas](updating-routes.md)
-   [Recibir notificación de cambios](receiving-notification-of-changes.md)
-   [Trabajar con próximos saltos](working-with-next-hops.md)
-   [Enumerar entradas de la tabla de enrutamiento](enumerating-routing-table-entries.md)
-   [Buscar información específica en la tabla de enrutamiento](finding-specific-information-in-the-routing-table.md)
-   [Mantenimiento de listas de Client-Specific](maintaining-client-specific-lists.md)
-   [Administrar identificadores](managing-handles.md)

 

 




