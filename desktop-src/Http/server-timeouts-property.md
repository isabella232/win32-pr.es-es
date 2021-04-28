---
title: Propiedad Tiempos de espera del servidor
description: Propiedad Tiempos de espera del servidor
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Http de la propiedad Tiempos de espera del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26fcd1376e8b7394a3a037bbbe00495466e32609
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090863"
---
# <a name="server-timeouts-property"></a>Propiedad Tiempos de espera del servidor

La API del servidor HTTP permite a las aplicaciones establecer los límites de tiempo de espera de conexión del servidor en una sesión de servidor o un grupo de direcciones URL. La propiedad tiempos de espera HTTP se usa para establecer todos los tiempos de espera en una base específica de la aplicación. Los **temporizadores IdleConnection** **y HeaderWait** también se pueden configurar en toda la API del servidor HTTP. Cuando los temporizadores se configuran en toda la API del servidor HTTP, se aplican a todas las aplicaciones de API de servidor HTTP del equipo y la configuración se conserva cuando se reinicia el servicio.

Para obtener más información sobre cómo configurar temporizadores, vea [Configurar los tiempos de espera específicos de la aplicación.](configuring-the-application-specific-timeouts.md)

Cuando los temporizadores no están configurados para un grupo de direcciones URL o una sesión de servidor, se aplican las configuraciones predeterminadas de la API del servidor HTTP.

El orden de cumplimiento del tiempo de espera es el siguiente:

1.  Los valores predeterminados para toda la API del servidor HTTP se aplican a todas las aplicaciones de API de servidor HTTP del equipo.
2.  Los tiempos de espera de sesión del servidor invalidan la configuración de toda la API del servidor HTTP, cuando se establece.
3.  La configuración del grupo de direcciones URL invalida las configuraciones de sesión del servidor, cuando se establece.

En la tabla siguiente se enumeran los límites de tiempo de espera de conexión predeterminados



| Temporizador           | Definición                                                                                                        | Valor predeterminado de LA API del servidor HTTP | Configurable como TODA LA API del servidor HTTP | Configurable como específico de la aplicación |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | La conexión expiró mientras estaba inactiva.                                                                        | 120 segundos                 | Yes                                  | Limitado                              |
| HeaderWait      | La conexión expiró mientras se esperaba que la API del servidor HTTP analizara el encabezado.                                 | 120 segundos                 | Yes                                  | Limitado                              |
| EntityBody      | La conexión expiró mientras esperaba a que llegara el cuerpo de la entidad de solicitud.                                       | 120 segundos                 | No                                   | Sí                                  |
| DrainEntityBody | La conexión expiró mientras se esperaba que la API del servidor HTTP purgara el cuerpo de la entidad en una Keep-Alive conexión. | 120 segundos                 | No                                   | Sí                                  |
| MinSendRate     | La conexión expiró porque la velocidad de envío de respuesta era más lenta que el valor predeterminado de 150 bytes/s.               | 150 segundos                 | No                                   | Sí                                  |
| RequestQueue    | La conexión expiró porque la solicitud permanecía en la cola de solicitudes antes de que la aplicación la seleccionara.     | 120 bytes/s           | No                                   | Sí                                  |



 

 

 




