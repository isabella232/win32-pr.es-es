---
title: Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects
description: Los objetos de la clase Container tienen un atributo otherWellKnownObjects que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propiedad otherWellKnownObjects
- propiedad otherWellKnownObjects, mediante para el enlace seguro para el cambio de nombre
- Active Directory, mediante, enlace, enlace seguro para el cambio de nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446f669adc9a59f9f8aba93e852546fe3991952857469d6f37978d9cf91a7666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695324"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects

Los objetos de la clase Container tienen un atributo **otherWellKnownObjects** que puede usar para asociar un GUID con el nombre distintivo (DN) de un objeto secundario en el contenedor. Si se mueve o cambia el nombre del objeto secundario, el servidor Active Directory actualiza el DN en el valor **otherWellKnownObjects** para ese objeto secundario. Esto permite el uso de la característica de enlace WKGUID para enlazar al objeto secundario mediante el GUID y el DN del contenedor en lugar del DN del objeto secundario.

El **atributo otherWellKnownObjects** es equivalente al atributo **wellKnownObjects,** salvo que las aplicaciones y los servicios pueden escribir un valor **otherWellKnownObjects,** pero solo el sistema puede escribir **wellKnownObjects**.

El uso del atributo **otherWellKnownObjects** y el enlace WKGUID es beneficioso en las siguientes situaciones en las que se requiere un enlace seguro para cambiar el nombre en relación con un objeto de contenedor específico.

Si un objeto contenedor contiene otros objetos importantes o si se puede cambiar el nombre o mover objetos importantes.

Si existen objetos importantes para cada instancia del objeto contenedor. Por ejemplo, el sistema usa el atributo **wellKnownObjects** de cada objeto **domainDNS** para almacenar un valor para el contenedor Users, que existe en cada instancia de un objeto **domainDNS.** Esto permite que las aplicaciones se enlacen al contenedor Usuarios de una manera segura para cambiar el nombre especificando el GUID conocido y el DN del contenedor **domainDNS.** Las aplicaciones pueden usar el atributo **otherWellKnownObjects** de un contenedor de forma similar.

Si necesita un enlace seguro para cambiar el nombre o la funcionalidad de búsqueda en los objetos importantes.

**Para agregar funcionalidades de búsqueda y enlace con seguridad de cambio de nombre**

1.  Agregue un valor a la **propiedad otherWellKnownObjects** del objeto contenedor cuando se cree el objeto importante dentro de ese contenedor. El valor contiene el GUID que representa el objeto conocido. Tenga en cuenta que este no es **objectGUID** y **distinguishedName** para ese objeto.
2.  Use la característica de enlace WKGUID para enlazar o buscar en el objeto importante.

El **otro atributoWellKnownObjects** puede tener varios valores y contiene las tuplas GUID/DN de objetos conocidos dentro de los contenedores en los que se establecen. El **atributo otherWellKnownObjects** tiene la sintaxis DNWithBinary en la que los valores tienen el formato siguiente:


```C++
B:<char count>:<well known GUID>:<object DN>
```



En este ejemplo, " char count " es el recuento de dígitos hexadecimales en " GUID conocido", que es 32 (número de dígitos hexadecimales en un GUID) para &lt; &gt; los &lt; &gt; **demásWellKnownObjects** y **wellKnownObjects**. "GUID &lt; &gt; conocido" es la representación de dígito hexadecimal del GUID conocido. " &lt; object DN &gt; " es el nombre distintivo del objeto representado por este valor WKO. El servidor mantiene la parte ObjectDN de cada **valor wellKnownObjects** y **otherWellKnownObjects** para que contenga el nombre distintivo actual del objeto especificado originalmente cuando se creó el valor.

Por ejemplo, si {df447b5e-aa5b-11d2-8d53-00c04f79ab81} es el GUID conocido del objeto MyObject en el contenedor MyContainer del dominio Fabrikam.com, el otro **valorwellKnownObjects** especificaría el GUID conocido y el DN de MyObject:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Para enlazar a este objeto, use la siguiente cadena de enlace WKGUID que especifica el GUID conocido del objeto y el DN del contenedor:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Después de enlazar a este objeto, puede usar las interfaces COM adsi para buscar, leer, modificar o eliminar el objeto.

Para obtener más información y un ejemplo de código que muestra cómo agregar un objeto al atributo **otherWellKnownObjects,** vea Ejemplo de código para [crear un objeto contenedor.](example-code-for-creating-a-container-object.md)

 

 




