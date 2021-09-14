---
description: Las ACE específicas del objeto se admiten para objetos de servicio de directorio (DS). Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: A ACE específicas del objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4212a0f7fe4eff7e38b41fe2636643c457cfeb51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244100"
---
# <a name="object-specific-aces"></a>A ACE específicas del objeto

Las ACE específicas del [*objeto se*](/windows/desktop/SecGloss/a-gly) admiten para objetos de servicio de directorio (DS). Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.




| GUID | Descripción | 
|------|-------------|
| <strong>ObjectType</strong> | Identifica uno de los siguientes elementos:<ul><li>Tipo de objeto secundario. La ACE controla el derecho para crear un tipo especificado de objeto secundario. Para obtener más información, vea <a href="controlling-child-object-creation-in-c--.md">Controlar la creación de objetos secundarios en C++.</a></li><li>Un conjunto de propiedades o una propiedad. La ACE controla el derecho a leer o escribir la propiedad o el conjunto de propiedades. Para obtener más información, vea <a href="aces-to-control-access-to-an-object-s-properties.md">ACE para controlar el acceso a las propiedades de un objeto</a>.</li><li>Derecho extendido. La ACE controla el derecho para realizar la operación asociada al derecho extendido.</li><li>Una escritura validada. La ACE controla el derecho a realizar determinadas operaciones de escritura. Estos permisos de escritura validados, definidos y expuestos en el Editor de ACL, proporcionan permisos para escrituras validadas de propiedades en lugar de escrituras de bajo nivel desactivadas de cualquier valor en una propiedad que se concede con un permiso de "propiedad de escritura".</li></ul> | 
| <strong>InheritedObjectType</strong> | Indica el tipo de objeto secundario que puede heredar la ACE. La herencia también se controla mediante las marcas de <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>herencia</strong></a>de la ACE_HEADER , así como por cualquier protección contra la herencia colocada en los objetos secundarios. Para obtener más información, vea <a href="ace-inheritance.md">Herencia ace</a>. | 




 

Se admiten tres tipos de AEE específicas del objeto.

> [!Note]  
> Actualmente no se admiten las ACE de objeto de alarma del sistema.

 



| Tipo                      | Descripción                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE de objeto de acceso denegado  | Se usa en una DACL para denegar a un administrador de confianza el acceso a una propiedad o propiedad establecida en el objeto o para limitar la herencia ace a un tipo especificado de objeto secundario. Usa la [**estructura ACCESS DENIED OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace)         |
| ACE de objeto con acceso permitido | Se usa en una DACL para permitir a un administrador de confianza el acceso a una propiedad o propiedad establecida en el objeto o para limitar la herencia ace a un tipo especificado de objeto secundario. Usa la [**estructura ACCESS ALLOWED OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)      |
| ACE de objeto de auditoría del sistema   | Se usa en una SACL para registrar los intentos de un administrador de confianza de acceder a una propiedad o propiedad establecida en el objeto o para limitar la herencia ace a un tipo especificado de objeto secundario. Usa la [**estructura SYSTEM AUDIT OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) |



 

Cualquier ACL que contenga una ACE específica del objeto debe usar la revisión ACL \_ REVISION \_ DS.

 

 
