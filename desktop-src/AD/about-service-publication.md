---
title: Acerca de la publicación de servicios
description: Un servicio es una aplicación que pone los datos u operaciones a disposición de los clientes de red. A menudo, un servicio se implementa como un servicio formal basado en Microsoft Win32, pero esto no es necesario.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3945107125df04bbdb862d476d0aba78711ba8f89622c732e0d6ae53d65d1eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840910"
---
# <a name="about-service-publication"></a>Acerca de la publicación de servicios

Un servicio es una aplicación que pone los datos u operaciones a disposición de los clientes de red. A menudo, un servicio se implementa como un servicio formal basado en Microsoft Win32, pero esto no es necesario.

La publicación del servicio es el acto de crear y mantener datos sobre una o varias instancias de un servicio determinado para que los clientes de red puedan encontrar y usar el servicio. La publicación de un servicio en Active Directory Domain Services permite a los clientes y administradores pasar de una vista centrada en el equipo del sistema distribuido a una vista centrada en el servicio.

**Microsoft Windows NT 3.51 y sistemas operativos posteriores:** Un sistema distribuido era un grupo de equipos que ejecutaba varios servicios. Para acceder a un servicio, una aplicación requería datos sobre qué equipos ofrecían el servicio.

**Windows 2000 Server, Windows 2000 Advanced Server y Windows Datacenter Server 2000:** Los servicios publican su existencia mediante Active Directory Domain Services objetos. Los objetos contienen información de enlace que las aplicaciones cliente usan para conectarse a instancias del servicio. Para acceder a un servicio, un cliente no necesita saber sobre equipos específicos: los objetos de un servidor Active Directory incluyen esta información. Un cliente consulta al servidor Active Directory un objeto que representa un servicio (denominado objeto de punto de conexión) y usa los datos de enlace del objeto para conectarse al servicio.

En la tabla siguiente se muestran ejemplos de enlaces.



| Servicio      | Enlace                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Servicio de archivos | Nombre UNC de un recurso compartido. Por ejemplo, \\ \\ "MyServer \\ MyshareName".                                                                                                                                                              |
| Servicio web  | dirección URL. Por ejemplo, " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Servicio RPC  | Enlace de llamada a procedimiento remoto (RPC): información codificada especial que se usa para conectarse al servidor RPC. Los enlaces RPC se pueden convertir a y desde cadenas con las API de RPC. Por ejemplo: "ncacn \_ ip \_ tcp:server.fabrikam.com". |



 

En un sistema distribuido, los equipos son motores y las entidades interesantes son los servicios que están disponibles. Desde la perspectiva del usuario, la identidad del equipo que proporciona un servicio determinado no es importante. Lo importante es acceder al propio servicio.

Este también es el caso de la administración de servicios. El administrador de una zona DNS determinada no está interesado en los equipos que ejecutan el servicio DNS; el administrador quiere administrar DNS. Es probable que haya varias instancias del servicio DNS, una de las cuales es autoritativa. Los equipos que admiten el servicio DNS no son importantes para el administrador de DNS. Lo importante es cómo administrar el servicio como un único recurso distribuido, no como procesos individuales que se ejecutan en equipos diferentes.

 

 




