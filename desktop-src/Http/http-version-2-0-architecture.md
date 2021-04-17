---
title: Arquitectura (API de servidor HTTP)
description: Los objetos de configuración de la sesión de servidor, la cola de solicitudes y el grupo de direcciones URL permiten a las aplicaciones configurar el servicio HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc7a07cb5e0439ed82421dd413aee3b6688bc0f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421806"
---
# <a name="architecture-http-server-api"></a>Arquitectura (API de servidor HTTP)

Los objetos de configuración de la sesión de servidor, la cola de solicitudes y el grupo de direcciones URL permiten a las aplicaciones configurar el servicio HTTP. Las propiedades establecidas en estos objetos invalidan las configuraciones predeterminadas de la API del servidor HTTP.

-   Sesión de servidor: el objeto de configuración de nivel superior que define las configuraciones de todos los grupos de direcciones URL creados en la sesión.
-   Grupo de direcciones URL: el grupo de direcciones URL, creado en la sesión de servidor, contiene un conjunto de direcciones URL que heredan las configuraciones establecidas en la sesión de servidor. Las configuraciones de grupo de direcciones URL invalidan las configuraciones de sesión de servidor cuando la aplicación la establece. El grupo de direcciones URL define una parte del espacio de nombres en el que la aplicación está escuchando y configura esa parte del espacio de nombres.
-   Cola de solicitudes: este objeto configura los valores específicos de la cola de solicitudes. Estas configuraciones se aplican a todas las direcciones URL de los grupos asociados a la cola de solicitudes.

En el diagrama siguiente se muestra la relación entre los objetos de configuración y la aplicación. Normalmente, se crea una sesión de un solo servidor para cada aplicación con uno o varios grupos de direcciones URL creados en ella. Las colas de solicitudes se crean independientemente del grupo de direcciones URL o la sesión del servidor. Los grupos de direcciones URL deben estar asociados a una cola de solicitudes para recibir solicitudes.

![relación entre los objetos de configuración y la aplicación](images/architecture.png)

La característica de cola de solicitudes con nombre de la API del servidor HTTP versión 2,0 permite que varios procesos de trabajo reciban solicitudes en una cola de solicitudes. La cola de solicitudes se crea mediante un proceso de controlador que identifica los procesos de trabajo a los que se ha concedido acceso a la cola de solicitudes. Para obtener más información, vea el tema [cola de solicitudes con nombre](named-request-queue.md) .

## <a name="property-configuration"></a>Configuración de propiedades

Para obtener más información sobre cómo establecer las propiedades de los objetos de configuración, vea los temas siguientes:

-   [Configuración de la cola de solicitudes](configuring-the-request-queue.md)
-   [Configurar la sesión de servidor](configuring-the-server-session.md)
-   [Configuración del grupo de direcciones URL](configuring-the-url-group.md)

En la tabla siguiente se enumeran las propiedades que se establecen en los objetos de configuración. Para obtener más información acerca de las configuraciones de propiedades, consulte el tema [configuración de las propiedades en http versión 2,0](configuring-properties-in-http-version-2-0.md) .



| Nombre           | Propiedad                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sesión de servidor | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Grupo de direcciones URL      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Cola de solicitudes  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





