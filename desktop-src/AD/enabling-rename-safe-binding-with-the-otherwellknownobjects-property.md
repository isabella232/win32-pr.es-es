---
title: Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects
description: Los objetos de la clase contenedor tienen un atributo otherWellKnownObjects que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propiedad otherWellKnownObjects
- propiedad otherWellKnownObjects, usar para el enlace con seguridad de cambio de nombre
- Active Directory, usar, enlazar y cambiar el nombre de enlaces seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268290"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects

Los objetos de la clase contenedor tienen un atributo **otherWellKnownObjects** que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor. Si el objeto secundario se mueve o se cambia de nombre, el servidor de Active Directory actualiza el DN en el valor **otherWellKnownObjects** para ese objeto secundario. Esto permite el uso de la característica de enlace WKGUID para enlazar con el objeto secundario mediante el GUID y el DN del contenedor en lugar del DN del objeto secundario.

El atributo **otherWellKnownObjects** es equivalente al atributo **wellKnownObjects** , salvo que las aplicaciones y los servicios pueden escribir un valor **otherWellKnownObjects** , pero solo el sistema puede escribir **wellKnownObjects**.

El uso del atributo **otherWellKnownObjects** y el enlace WKGUID es beneficioso en las siguientes situaciones en las que se requiere un enlace con seguridad de cambio de nombre en relación con un objeto contenedor específico.

Si un objeto contenedor contiene otros objetos importantes, o si se puede cambiar el nombre o la ubicación de los objetos importantes.

Si existen objetos importantes para cada instancia del objeto contenedor. Por ejemplo, el sistema utiliza el atributo **wellKnownObjects** de cada objeto **domainDNS** para almacenar un valor para el contenedor usuarios, que existe en cada instancia de un objeto **domainDNS** . Esto permite que las aplicaciones se enlacen al contenedor de usuarios en una forma segura para cambiar el nombre mediante la especificación del GUID conocido y el DN del contenedor **domainDNS** . Las aplicaciones pueden usar el atributo **otherWellKnownObjects** de un contenedor de forma similar.

Si necesita una capacidad de enlace y/o búsqueda segura para el cambio de nombre en los objetos importantes.

**Para agregar funcionalidades de búsqueda y enlace con seguridad de cambio de nombre**

1.  Agregue un valor a la propiedad **otherWellKnownObjects** del objeto contenedor cuando se cree el objeto importante dentro de ese contenedor. El valor contiene el GUID que representa el objeto conocido. Tenga en cuenta que esto no es el **objectGUID** y el **distinguishedName** para ese objeto.
2.  Use la característica de enlace WKGUID para enlazar con el objeto importante o buscar en él.

El atributo **otherWellKnownObjects** puede tener varios valores y contiene las tuplas GUID/DN de objetos conocidos en los contenedores en los que se establecen. El atributo **otherWellKnownObjects** tiene la sintaxis DNWithBinary en la que los valores tienen el formato siguiente:


```C++
B:<char count>:<well known GUID>:<object DN>
```



En este ejemplo, " &lt; Char Count &gt; " es el recuento de dígitos hexadecimales en " &lt; GUID conocido &gt; ", que es 32 (número de dígitos hexadecimales en un GUID) para **otherWellKnownObjects** y **wellKnownObjects**. " &lt; GUID conocido &gt; " es la representación de dígitos hexadecimales del GUID conocido. " &lt; DN &gt; del objeto" es el nombre distintivo del objeto representado por este valor de WKO. El servidor mantiene la parte Dnobjeto de cada valor **wellKnownObjects** y **otherWellKnownObjects** para que contenga el nombre distintivo actual del objeto que se especificó originalmente cuando se creó el valor.

Por ejemplo, si {df447b5e-AA5B-11D2-8d53-00c04f79ab81} es el GUID conocido del objeto DataObject en el contenedor de alcontainer en el dominio Fabrikam.com, el valor **otherWellKnownObjects** especificaría el GUID conocido y el DN de DataObject:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Para enlazar a este objeto, use la siguiente cadena de enlace WKGUID que especifica el GUID conocido del objeto y el DN del contenedor:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Después de enlazar a este objeto, puede usar las interfaces COM ADSI para buscar, leer, modificar o eliminar el objeto.

Para obtener más información y un ejemplo de código que muestra cómo agregar un objeto al atributo **otherWellKnownObjects** , vea el [código de ejemplo para crear un objeto contenedor](example-code-for-creating-a-container-object.md).

 

 




