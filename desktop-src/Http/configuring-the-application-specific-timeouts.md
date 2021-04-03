---
title: Configurar los tiempos de espera específicos de la aplicación
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurar los tiempos de espera específicos de la aplicación HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075661"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configurar los tiempos de espera específicos de la aplicación

La configuración de toda la API del servidor HTTP se aplica a todas las sesiones del servidor y a los grupos de direcciones URL del equipo. La aplicación puede invalidar estas configuraciones estableciendo los valores de tiempo de espera específicos de la aplicación. Los tiempos de espera de la sesión del servidor invalidan los tiempos de espera de la API del servidor HTTP y se aplican a todos los grupos de direcciones URL creados en ellos. Al configurar la propiedad timeouts en un grupo de direcciones URL, se invalidan los tiempos de espera de la sesión del servidor para todas las direcciones URL del grupo.

Si se especifica cero para cualquiera de los temporizadores de la estructura de [**información de límite de tiempo de espera de http \_ \_ \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) para un grupo de direcciones URL, la API del servidor http volverá a los tiempos de espera de la sesión del servidor, si existen, o la configuración predeterminada de la API del servidor http si los tiempos de espera de la sesión del servidor no existen. Por ejemplo, si la propiedad de tiempo de espera del servidor se encuentra en un grupo de direcciones URL y el temporizador de **EntityBody** es cero, se utiliza el tiempo de espera de la sesión del servidor. Si no se establece la propiedad timeouts en una sesión de servidor, se utiliza la configuración predeterminada de la API del servidor HTTP. Para deshabilitar un temporizador, establezca el valor en **MAXUSHORT**, excepto en el temporizador de **MinSendRate** que se establece en **MAXULONG**.

La API del servidor HTTP solo puede configurar el **HeaderWait** específico de la aplicación y los temporizadores de **IdleConnection** solo se aplican después de que se haya recibido la primera solicitud. Antes de que se reciba la primera solicitud, se aplican los valores de tiempo de espera de la API del servidor HTTP. Una vez que la primera solicitud llega y está asociada a una cola de solicitudes, se pueden aplicar los temporizadores de **HeaderWait** y **IdleConnection** específicos de la aplicación. Los temporizadores específicos de la aplicación se aplican a todas las solicitudes posteriores que llegan a la cola de solicitudes para una conexión Keep-Alive.

Para obtener más información acerca de cómo configurar temporizadores, consulte los temas [configurar el grupo de direcciones URL](configuring-the-url-group.md) y [configurar la sesión de servidor](configuring-the-server-session.md) .

 

 




