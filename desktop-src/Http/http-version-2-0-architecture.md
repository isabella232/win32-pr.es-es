---
title: Arquitectura (API de servidor HTTP)
description: La sesión del servidor, la cola de solicitudes y los objetos de configuración del grupo de direcciones URL permiten a las aplicaciones configurar el servicio HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3905a27708c87c43e141dd4cf8d84b2f0e7e66bc4dd189440733321ee951a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997115"
---
# <a name="architecture-http-server-api"></a>Arquitectura (API de servidor HTTP)

La sesión del servidor, la cola de solicitudes y los objetos de configuración del grupo de direcciones URL permiten a las aplicaciones configurar el servicio HTTP. Las propiedades establecidas en estos objetos invalidan las configuraciones predeterminadas de la API de servidor HTTP.

-   Sesión de servidor: el objeto de configuración de nivel superior que define las configuraciones de todos los grupos de direcciones URL creados en la sesión.
-   Grupo de direcciones URL: el grupo de direcciones URL, creado en la sesión del servidor, contiene un conjunto de direcciones URL que heredan las configuraciones establecidas en la sesión del servidor. Las configuraciones de grupo de direcciones URL invalidan las configuraciones de sesión del servidor cuando la aplicación la establece. El grupo de direcciones URL define una parte del espacio de nombres en el que escucha la aplicación y configura esa parte del espacio de nombres.
-   Cola de solicitudes: este objeto configura valores específicos de la cola de solicitudes. Estas configuraciones se aplican a todas las direcciones URL de los grupos asociados a la cola de solicitudes.

En el diagrama siguiente se muestra la relación entre los objetos de configuración y la aplicación. Normalmente, se crea una sesión de servidor único para cada aplicación con uno o varios grupos de direcciones URL creados en ella. Las colas de solicitudes se crean independientemente del grupo de direcciones URL o la sesión del servidor. Los grupos de direcciones URL deben estar asociados a una cola de solicitudes para recibir solicitudes.

![relación entre los objetos de configuración y la aplicación](images/architecture.png)

La característica cola de solicitudes con nombre de la API del servidor HTTP versión 2.0 permite que varios procesos de trabajo reciban solicitudes en una cola de solicitudes. La cola de solicitudes se crea mediante un proceso de controlador que identifica los procesos de trabajo a los que se concedió acceso a la cola de solicitudes. Para obtener más información, vea el [tema Cola de solicitudes con](named-request-queue.md) nombre

## <a name="property-configuration"></a>Configuración de propiedades

Para obtener más información sobre cómo establecer propiedades en los objetos de configuración, vea los temas siguientes:

-   [Configuración de la cola de solicitudes](configuring-the-request-queue.md)
-   [Configuración de la sesión de servidor](configuring-the-server-session.md)
-   [Configuración del grupo de direcciones URL](configuring-the-url-group.md)

En la tabla siguiente se enumeran las propiedades que se establecen en los objetos de configuración. Para obtener más información sobre las configuraciones de propiedades, vea el tema [Configuring Properties in HTTP Version 2.0](configuring-properties-in-http-version-2-0.md) .



| Nombre           | Propiedad                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sesión de servidor | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Grupo de direcciones URL      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Cola de solicitudes  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





