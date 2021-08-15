---
title: Proxy de aplicación web
description: Proxy de aplicación web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211330"
---
# <a name="web-application-proxy"></a>Proxy de aplicación web

## <a name="platform"></a>Plataforma

**Servidores:** Windows Server 2012 R2  






## <a name="description"></a>Descripción

En Windows Server 2012 R2, agregamos un nuevo servicio denominado Web Application Proxy bajo el rol acceso remoto que permite a los administradores publicar aplicaciones para el acceso externo. Este servicio actúa como un proxy inverso y como un proxy Servicios de federación de Active Directory (AD FS) (AD FS). De hecho, este servicio reemplaza el AD FS proxy como se conocía en Windows Server 2012.

Con web Application Proxy, una organización puede hacer que los recursos web locales estén disponibles para el acceso externo y, al mismo tiempo, administrar el riesgo de este acceso mediante el control de las directivas de autenticación y autorización en el AD FS.

## <a name="manifestation"></a>Manifestación

El AD FS proxy de Servicios de federación de Active Directory (AD FS) ya no está bajo el rol Servicios de federación de Active Directory (AD FS) (AD FS), pero se ha reemplazado por el servicio web Application Proxy en el rol de acceso remoto. Esto representa una expansión del servicio de proxy AD FS mediante la inclusión de la funcionalidad de proxy inverso para la publicación de aplicaciones.

## <a name="solution"></a>Solución

Para acceder a la Application Proxy web, los administradores pueden ir a Administrador del servidor y agregar un nuevo servicio de rol o rol. El administrador encontrará la aplicación web Application Proxy el rol Acceso remoto.

## <a name="resources"></a>Recursos

-   [Guía de soluciones](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 