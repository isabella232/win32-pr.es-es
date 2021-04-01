---
description: Las ACE específicas del objeto son compatibles con los objetos del servicio de directorio (DS). Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE específicas del objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082997"
---
# <a name="object-specific-aces"></a>ACE específicas del objeto

Las [*ACE*](/windows/desktop/SecGloss/a-gly) específicas del objeto son compatibles con los objetos del servicio de directorio (DS). Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ObjectType</strong></td>
<td>Identifica una de las siguientes opciones:
<ul>
<li>Tipo de objeto secundario. La ACE controla la derecha para crear un tipo especificado de objeto secundario. Para obtener más información, vea <a href="controlling-child-object-creation-in-c--.md">controlar la creación de objetos secundarios en C++</a>.</li>
<li>Una propiedad o un conjunto de propiedades. La ACE controla el derecho para leer o escribir la propiedad o el conjunto de propiedades. Para obtener más información, vea <a href="aces-to-control-access-to-an-object-s-properties.md">ACE para controlar el acceso a las propiedades de un objeto</a>.</li>
<li>Un derecho extendido. La ACE controla el derecho para realizar la operación asociada con el derecho extendido.</li>
<li>Una escritura validada. La ACE controla el derecho para realizar ciertas operaciones de escritura. Estos permisos de escritura validados, que se definen y exponen en el editor ACL, proporcionan permisos para la escritura validada de propiedades en lugar de escrituras de bajo nivel no comprobadas de cualquier valor a una propiedad que se concede con un &quot; permiso de propiedad de escritura &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>InheritedObjectType</strong></td>
<td>Indica el tipo de objeto secundario que puede heredar la ACE. La herencia también se controla mediante los marcadores de herencia en el <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, así como cualquier protección contra la herencia colocada en los objetos secundarios. Para obtener más información, vea <a href="ace-inheritance.md">herencia de ACE</a>.</td>
</tr>
</tbody>
</table>



 

Se admiten tres tipos de ACE específicas del objeto.

> [!Note]  
> No se admiten las ACE de objetos de alarma del sistema actualmente.

 



| Tipo                      | Descripción                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE de objeto de acceso denegado  | Se usa en una DACL para denegar el acceso de un administrador de confianza a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario. Utiliza la estructura [**ACE de objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .         |
| ACE de objeto con permiso de acceso | Se usa en una DACL para permitir que un administrador de confianza tenga acceso a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario. Utiliza la [**estructura \_ \_ \_ ACE del objeto de acceso permitido**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .      |
| ACE del objeto de auditoría del sistema   | Se usa en una SACL para registrar los intentos de un administrador de confianza de obtener acceso a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario. Utiliza la [**estructura \_ \_ \_ ACE del objeto de auditoría del sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) . |



 

Todas las ACL que contengan una ACE específica del objeto deben usar la revisión de la ACL de revisión \_ \_ DS.

 

 
