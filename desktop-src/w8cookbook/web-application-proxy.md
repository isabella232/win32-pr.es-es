---
title: Proxy de aplicación web
description: Proxy de aplicación web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104149686"
---
# <a name="web-application-proxy"></a>Proxy de aplicación web

## <a name="platform"></a>Plataforma

**Servidores:** Windows Server 2012 R2  






## <a name="description"></a>Descripción

En Windows Server 2012 R2, se ha agregado un nuevo servicio denominado proxy de aplicación web en el rol de acceso remoto que permite a los administradores publicar aplicaciones para el acceso externo. Este servicio actúa como proxy inverso y como proxy de Servicios de federación de Active Directory (AD FS) (AD FS). De hecho, este servicio reemplaza el servicio de proxy de AD FS como se conocía en Windows Server 2012.

Con el proxy de aplicación Web, una organización puede hacer que los recursos web locales estén disponibles para el acceso externo al mismo tiempo que administra el riesgo de este acceso mediante el control de las directivas de autenticación y autorización en el AD FS.

## <a name="manifestation"></a>Manifestación

El servicio de proxy de AD FS ya no se encuentra en el rol de Servicios de federación de Active Directory (AD FS) (AD FS), pero se ha reemplazado por el proxy de aplicación web en el rol de acceso remoto. Esto representa una expansión del servicio de proxy de AD FS mediante la inclusión de la funcionalidad de proxy inverso para la publicación de aplicaciones.

## <a name="solution"></a>Solución

Para tener acceso al proxy de aplicación Web, los administradores pueden ir a Administrador del servidor y agregar un nuevo rol o servicio de rol. El administrador encontrará el proxy de aplicación web en el rol de acceso remoto.

## <a name="resources"></a>Recursos

-   [Guía de soluciones](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 