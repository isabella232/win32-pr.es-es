---
title: Configuración de los tiempos de espera específicos de la aplicación
description: Configuración de los tiempos de espera específicos de la aplicación
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configuración de los tiempos de espera específicos de la aplicación HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722d44c1377a3bee22a88fe92f0f5aed272c08f0b0a6645361c4e03816f408fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950884"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configuración de los tiempos de espera específicos de la aplicación

La configuración de toda la API del servidor HTTP se aplica a todas las sesiones de servidor y grupos de direcciones URL del equipo. La aplicación puede invalidar estas configuraciones estableciendo los valores de tiempo de espera específicos de la aplicación. Los tiempos de espera de la sesión del servidor invalidan los tiempos de espera de la API del servidor HTTP y se aplican a todos los grupos de direcciones URL creados en ellos. La configuración de la propiedad timeouts en un grupo de direcciones URL invalida los tiempos de espera de sesión del servidor para todas las direcciones URL del grupo.

Si se especifica cero para cualquiera de los temporizadores de la estructura [**HTTP \_ TIMEOUT LIMIT \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) para un grupo de direcciones URL, la API del servidor HTTP se revierte a los tiempos de espera de sesión del servidor, si existen, o a la configuración predeterminada de LA API del servidor HTTP si no existen tiempos de espera de sesión del servidor. Por ejemplo, cuando la propiedad de tiempo de espera del servidor está presente en un grupo de direcciones URL y el temporizador **de EntityBody** es cero, se usa el tiempo de espera de la sesión del servidor. Si la propiedad timeouts no está establecida en una sesión de servidor, se usa la configuración predeterminada de LA API del servidor HTTP. Para deshabilitar un temporizador, establezca el valor en **MAXUSHORT**, excepto para el temporizador **MinSendRate** que se establece en **MAXULONG.**

La API del servidor HTTP solo puede configurar **headerWait** específico de la aplicación y los temporizadores **IdleConnection** solo son efectivos después de recibir la primera solicitud. Antes de recibir la primera solicitud, se aplican los valores de tiempo de espera de toda la API del servidor HTTP. Una vez que llega la primera solicitud y está asociada a una cola de solicitudes, se pueden aplicar los temporizadores **HeaderWait** e **IdleConnection** específicos de la aplicación. Los temporizadores específicos de la aplicación se aplican a todas las solicitudes posteriores que llegan a la cola de solicitudes para una conexión keep-alive.

Para obtener más información sobre cómo configurar temporizadores, vea los temas Configurar el grupo [de direcciones URL](configuring-the-url-group.md) y Configurar la sesión [del](configuring-the-server-session.md) servidor.

 

 




