---
title: Herencia y delegación de administración
description: Describe AD DS compatibilidad con la herencia de permisos en el árbol de objetos y también la herencia específica del objeto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- herencia de administración y delegación Active Directory
- Active Directory Active Directory herencia ,permissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b48ff4d913cbd8bf16f7b2c67adf86d61515298dcac267291641d30504e1e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187528"
---
# <a name="inheritance-and-delegation-of-administration"></a>Herencia y delegación de administración

Active Directory Domain Services admite la herencia de permisos en el árbol de objetos para permitir que las tareas de administración se realicen en niveles superiores del árbol. Esto permite a los administradores configurar permisos heredables en objetos cercanos a la raíz, como el dominio y las unidades organizativas, y distribuir esos permisos a varios objetos del árbol.

La herencia se puede establecer por ACE. En la tabla siguiente se enumeran las marcas que se pueden especificar en **AceFlags** para controlar la herencia de la ACE.



| Marca                                                     | Descripción                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ INHERIT \_ ACE**<br/>                | Hace que la ACE se herede en el árbol.<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ NO \_ PROPAGATE \_ INHERIT \_ ACE**<br/> | Hace que la ACE se herede solo un nivel en el árbol.<br/>                                                                      |
| **ADS \_ ACEFLAG \_ INHERIT \_ ONLY \_ ACE**<br/>          | Hace que la ACE se ignore en el objeto en el que se especifica, solo se herede y sea eficaz donde se ha heredado.<br/> |



 

Además de establecer la herencia, Active Directory Domain Services admite la herencia específica del objeto. Esto permite que las ACE heredables se hereden en el árbol, pero solo sean eficaces en un tipo específico de objeto. Esto es muy útil para delegar la administración. Por ejemplo, esto se puede usar para establecer una ACE heredable específica del objeto en una unidad organizativa que permita a un grupo tener control total sobre todos los objetos de usuario de la unidad organizativa, pero nada más. Por lo tanto, la administración de los usuarios de esa unidad organizativa se delega en los usuarios de ese grupo.

### <a name="delegating-service-administration-with-security-groups"></a>Delegación de la administración de servicios con grupos de seguridad

Use grupos de seguridad para definir y delegar roles administrativos asociados al servidor de aplicaciones. Por ejemplo, el servicio puede estar asociado a un grupo MyService Administrators. Los usuarios identificados como administradores de MyService se agregarán al grupo Administradores de MyService. El programa de instalación de MyService puede establecer acl en el directorio para permitir a los administradores de MyService permisos suficientes para leer o escribir atributos relacionados con MyService o crear objetos específicos de MyService, por ejemplo.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Roles en grupos de seguridad para equipos que ejecutan el servicio

Use grupos de seguridad para definir el conjunto de equipos a los que se concede acceso a los objetos del servicio en el directorio. Por ejemplo, el servicio puede estar asociado a un grupo MyService Servers. Todos los equipos que ejecutan el servidor MyService se agregan al grupo Servidores de MyService y a este grupo se le puede dar acceso a las partes del directorio donde los servidores MyService necesitan leer y escribir datos. El programa de instalación de MyService puede establecer acl en el directorio para habilitar los servidores de MyService con permisos suficientes para leer y escribir atributos relacionados con MyService o crear objetos específicos de MyService, por ejemplo.

 

 





