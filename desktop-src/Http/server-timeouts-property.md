---
title: Propiedad tiempos de espera del servidor
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Tiempo de espera del servidor (propiedad) HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418861"
---
# <a name="server-timeouts-property"></a>Propiedad tiempos de espera del servidor

La API del servidor HTTP permite a las aplicaciones establecer los límites de tiempo de espera de conexión del servidor en una sesión de servidor o un grupo de direcciones URL. La propiedad tiempo de espera de HTTP se usa para establecer todos los tiempos de espera en función de la aplicación. Los temporizadores **IdleConnection** y **HeaderWait** también se pueden configurar en todo el servidor HTTP de la API. Cuando los temporizadores están configurados en la API del servidor HTTP, se aplican a todas las aplicaciones de API del servidor HTTP en el equipo y la configuración se conserva cuando se reinicia el servicio.

Para obtener más información sobre la configuración de temporizadores, vea [configurar los tiempos de espera específicos de la aplicación](configuring-the-application-specific-timeouts.md).

Cuando los temporizadores no están configurados para un grupo de direcciones URL o una sesión de servidor, se aplican las configuraciones predeterminadas de la API del servidor HTTP.

El orden de cumplimiento del tiempo de espera es el siguiente:

1.  Los valores predeterminados generales de la API del servidor HTTP se aplican a todas las aplicaciones de API del servidor HTTP del equipo.
2.  Los tiempos de espera de la sesión del servidor invalidan la configuración de toda la API del servidor HTTP, cuando se establece.
3.  La configuración del grupo de direcciones URL invalida las configuraciones de sesión del servidor, cuando se establece.

En la tabla siguiente se enumeran los límites de tiempo de espera de conexión predeterminados



| Temporizador           | Definición                                                                                                        | HTTP Server API predeterminada | Configurable como API de servidor HTTP de ancho | Configurable como específico de la aplicación |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | La conexión expiró mientras se mantiene inactiva.                                                                        | 120 s                 | Sí                                  | Limitado                              |
| HeaderWait      | La conexión expiró mientras se esperaba a que la API del servidor HTTP analizara el encabezado.                                 | 120 s                 | Sí                                  | Limitado                              |
| EntityBody      | La conexión expiró mientras se esperaba a que llegara el cuerpo de la entidad de solicitud.                                       | 120 s                 | No                                   | Sí                                  |
| DrainEntityBody | La conexión expiró mientras se esperaba a que la API del servidor HTTP DRENASE el cuerpo de la entidad en una conexión de Keep-Alive. | 120 s                 | No                                   | Sí                                  |
| MinSendRate     | La conexión expiró porque la velocidad de envío de respuesta era más lenta que el valor predeterminado de 150 bytes por segundo.               | 150 s                 | No                                   | Sí                                  |
| RequestQueue    | La conexión expiró porque la solicitud permaneció en la cola de solicitudes antes de que la aplicación la haya seleccionado.     | 120 bytes por segundo           | No                                   | Sí                                  |



 

 

 




