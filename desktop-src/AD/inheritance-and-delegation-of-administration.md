---
title: Herencia y delegación de la administración
description: Describe AD DS compatibilidad con la herencia de permisos en el árbol de objetos y también la herencia específica del objeto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- herencia y delegación de administración Active Directory
- Active Directory de Active Directory, herencia de permisos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268278"
---
# <a name="inheritance-and-delegation-of-administration"></a>Herencia y delegación de la administración

Active Directory Domain Services admite la herencia de permisos en el árbol de objetos para permitir que las tareas de administración se realicen en niveles superiores del árbol. Esto permite a los administradores configurar permisos heredables en objetos cercanos a la raíz, como el dominio y las unidades organizativas, y tener esos permisos distribuidos a diversos objetos del árbol.

La herencia se puede establecer por ACE. En la tabla siguiente se enumeran las marcas que se pueden especificar en **AceFlags** para controlar la herencia de la ACE.



| Marca                                                     | Descripción                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE de \_ herencia de ACEFLAG de ADS \_**<br/>                | Hace que la ACE se herede en el árbol.<br/>                                                                                     |
| **ACEFLAG de anuncios \_ \_ no \_ propagar la \_ ACE de herencia \_**<br/> | Hace que la ACE se herede solo en un nivel del árbol.<br/>                                                                      |
| **ACEFLAG de anuncios \_ \_ solo heredan \_ \_ ACE**<br/>          | Hace que la ACE se omita en el objeto en el que se especifica, solo se puede heredar y ser efectiva en la que se ha heredado.<br/> |



 

Además de establecer la herencia, Active Directory Domain Services admite la herencia específica del objeto. Esto permite que las ACE heredables se hereden en el árbol, pero solo se aplican a un tipo específico de objeto. Esto es muy útil para delegar la administración. Por ejemplo, se puede usar para establecer una ACE heredable específica de un objeto en una unidad organizativa que permita que un grupo tenga control total sobre todos los objetos de usuario en la unidad organizativa, pero nada más. Por lo tanto, la administración de los usuarios de esa unidad organizativa se delega a los usuarios de ese grupo.

### <a name="delegating-service-administration-with-security-groups"></a>Delegación de la administración de servicios con grupos de seguridad

Use grupos de seguridad para definir y delegar roles administrativos asociados con el servidor de aplicaciones. Por ejemplo, el servicio puede estar asociado a un grupo administradores de servicios. Los usuarios que se identifican como administradores de servicio se agregarán al grupo administradores de el servicio. El programa de instalación de en el servicio puede establecer ACL en el directorio para permitir que los administradores de el servicio tengan suficientes permisos para leer o escribir atributos relacionados con el servicio, o para crear objetos específicos de este servicio, por ejemplo.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Roles en grupos de seguridad para equipos que ejecutan el servicio

Use grupos de seguridad para definir el conjunto de equipos a los que se concede acceso a los objetos del servicio en el directorio. Por ejemplo, el servicio puede estar asociado a un grupo de servidores de servicio. Todos los equipos que ejecutan el servidor de servicio se agregan al grupo de servidores de servicio y a este grupo se le puede conceder acceso a partes del directorio en el que los servidores de servicio necesitan leer o escribir datos. El programa de instalación de en el servicio puede establecer ACL en el directorio para habilitar los servidores de servicio de los permisos suficientes para leer y escribir los atributos relacionados con el servicio, o para crear objetos específicos del servicio, por ejemplo.

 

 





