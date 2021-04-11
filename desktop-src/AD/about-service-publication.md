---
title: Acerca de la publicación de servicio
description: Un servicio es una aplicación que hace que los datos u operaciones estén disponibles para los clientes de red. A menudo, un servicio se implementa como un servicio formal basado en Microsoft Win32, pero esto no es necesario.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993808"
---
# <a name="about-service-publication"></a>Acerca de la publicación de servicio

Un servicio es una aplicación que hace que los datos u operaciones estén disponibles para los clientes de red. A menudo, un servicio se implementa como un servicio formal basado en Microsoft Win32, pero esto no es necesario.

La publicación de servicio es el acto de crear y mantener datos sobre una o varias instancias de un servicio determinado para que los clientes de red puedan encontrar y usar el servicio. La publicación de un servicio en Active Directory Domain Services permite a los clientes y administradores pasar de una vista centrada en el equipo del sistema distribuido a una vista centrada en el servicio.

**Sistemas operativos Microsoft Windows NT 3,51 y versiones posteriores:** Un sistema distribuido era un grupo de equipos que ejecutan varios servicios. Para tener acceso a un servicio, una aplicación necesitaba datos sobre qué equipos ofrecían el servicio.

**Windows 2000 Server, windows 2000 Advanced Server y windows 2000 Datacenter Server:** Los servicios publican su existencia con objetos de Active Directory Domain Services. Los objetos contienen información de enlace que las aplicaciones cliente utilizan para conectarse a las instancias del servicio. Para tener acceso a un servicio, no es necesario que un cliente conozca los equipos específicos: los objetos de un servidor de Active Directory incluyen esta información. Un cliente consulta el servidor de Active Directory para un objeto que representa un servicio (denominado objeto de punto de conexión) y utiliza los datos de enlace del objeto para conectarse al servicio.

En la tabla siguiente se muestran ejemplos de enlaces.



| Servicio      | Enlace                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Servicio de archivos | Nombre UNC de un recurso compartido. Por ejemplo, " \\ \\ \\ MyshareName".                                                                                                                                                              |
| Servicio web  | dirección URL. Por ejemplo, " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Servicio RPC  | Enlace de llamada a procedimiento remoto (RPC): información especial codificada utilizada para conectarse al servidor RPC. Los enlaces RPC se pueden convertir en cadenas y a partir de ellas con las API de RPC. Por ejemplo: "ncacn \_ IP \_ TCP:Server. fabrikam. com". |



 

En un sistema distribuido, los equipos son motores y las entidades interesantes son los servicios que están disponibles. Desde la perspectiva del usuario, no es importante la identidad del equipo que proporciona un servicio determinado. Lo que es importante es el acceso al propio servicio.

Este también es el caso de la administración de servicios. El administrador de una zona DNS determinada no está interesado en los equipos que ejecutan el servicio DNS; el administrador desea administrar DNS. Probablemente habrá varias instancias del servicio DNS, una de las cuales es autoritativa. Los equipos que admiten el servicio DNS no son importantes para el administrador de DNS. Lo importante es cómo administrar el servicio como un solo recurso distribuido, no como procesos individuales que se ejecutan en equipos diferentes.

 

 




