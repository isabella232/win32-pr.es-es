---
title: Enlazar a objetos de Well-Known mediante WKGUID
description: En este tema se muestra cómo enlazar a objetos mediante la cadena de enlace WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Enlazar a objetos de Well-Known mediante WKGUID AD
- Active Directory, usar, enlazar, usar WKGUID para enlazar a objetos conocidos
- objetos conocidos de AD
- objetos conocidos de AD, enlace al uso de WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789634"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Enlazar a objetos de Well-Known mediante WKGUID

Los contenedores pueden tener uno o varios subobjetos importantes a los que se puede cambiar el nombre o que se pueden desplace. Puede ser difícil realizar un seguimiento de estos subobjetos y crear cadenas de enlace correctas para ellos, especialmente si se les cambia el nombre o se mueven.

Para admitir el enlace con seguridad de cambio de nombre a estos objetos dentro de estos contenedores, Active Directory Domain Services tienen dos atributos: **wellKnownObjects** y **otherWellKnownObjects**. Estos atributos tienen una sintaxis de atributo de \_ DN ADSTYPE \_ con \_ binario. Permiten varios valores y contienen las tuplas GUID/DN de objetos conocidos en los contenedores en los que se establecen. El servidor de Active Directory mantiene la parte del nombre distintivo de cada entrada de **wellKnownObjects** y **otherWellKnownObjects** para que contenga el nombre distintivo actual del objeto especificado cuando se creó la entrada.

La propiedad **otherWellKnownObjects** se puede establecer y usar en cualquier objeto.

La propiedad **wellKnownObjects** se utiliza en los contenedores domainDNS y Configuration. La propiedad **wellKnownObjects** es una propiedad solo del sistema y solo puede ser modificada por el sistema operativo.

El contenedor **domainDNS** tiene los siguientes objetos conocidos:

-   Usuarios
-   Computers
-   System
-   Controladores de dominio
-   Infraestructura
-   Objetos eliminados
-   Perdido y encontrado

El contenedor de configuración tiene el objeto conocido: objetos eliminados.

Estos objetos se encuentran en todos los contenedores de **domainDNS** y configuración de un servicio dominio de Active Directory.

Puede enlazar a un objeto conocido mediante el formato de enlace WKGUID. El enlace con WKGUID solo se admite en Active Directory Domain Services, es decir, el proveedor LDAP.

> [!IMPORTANT]
> Use siempre el formato de enlace WKGUID para enlazar con los objetos conocidos, como se indicó anteriormente, en los contenedores de configuración y dominio. Esto garantiza que estos contenedores se pueden enlazar a incluso si se mueven o cambian de nombre.

 

El formato de la cadena de enlace WKGUID es el siguiente:


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



" &lt; nombre &gt; del servidor" es el nombre del servidor de directorio. El " &lt; nombre del servidor &gt; " es opcional.

" &lt; Xxxxx &gt; " es la representación de cadena del valor hexadecimal del GUID que representa el objeto conocido. La cadena GUID se especifica en el formulario "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" y no es de la misma forma que la cadena GUID generada por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , que tiene la forma "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}". Para obtener más información y un ejemplo de código que muestra cómo crear una cadena enlazable desde un GUID, vea el [código de ejemplo para crear una representación de cadena enlazable de un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).

Para enlazar a un objeto especificado en **otherWellKnownObjects** en un objeto, especifique " &lt; xxxxx &gt; " como forma de cadena de enlace del GUID de objeto conocido del objeto. Para obtener más información, vea [leer el objectGUID de un objeto y crear una representación de cadena del GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md). Para obtener más información sobre cómo establecer la propiedad **otherWellKnownObjects** en objetos, vea [Habilitar el enlace de Rename-Safe con la propiedad otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Para enlazar a un objeto especificado en **wellKnownObjects** en domainDNS o en contenedores de configuración, especifique " &lt; xxxxx &gt; " como una de las constantes siguientes, que se enumeran en la tabla siguiente, tal como se define en ntdsapi. h.



| Contenedor          | Identificador GUID                         |
|--------------------|-----------------------------------------|
| Usuarios              | contenedor de usuarios de GUID \_ \_ \_ W               |
| Computers          | \_contenedor de calculadores GUID \_ \_ W            |
| System             | \_contenedor de sistemas GUID \_ \_ W             |
| Controladores de dominio | \_contenedor de controladores de dominio GUID \_ \_ \_ W |
| Infraestructura     | \_contenedor de infraestructura GUID \_ \_ W      |
| Objetos eliminados    | \_contenedor de objetos eliminados de GUID \_ \_ \_ W    |
| Perdido y encontrado     | contenedor de GUID \_ LOSTANDFOUND \_ \_ W        |



 

Por ejemplo, para enlazar con el contenedor de usuario en un dominio, especifique el **\_ contenedor de usuarios GUID \_ \_ W** como " &lt; xxxxx &gt; ".

" &lt; DN &gt; de contenedor" es el nombre distintivo del objeto contenedor que tiene este objeto representado como un valor en su propiedad **wellKnownObjects** . Por ejemplo, para enlazar con el contenedor usuarios de un dominio, especifique el nombre distintivo del dominio como el " &lt; DN del contenedor &gt; ".

Por ejemplo, para enlazar con el contenedor de usuarios del dominio Fabrikam.com, use la siguiente cadena de enlace.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Para obtener más información y un ejemplo de código que muestra cómo enlazar a un GUID conocido, vea [código de ejemplo para enlazar a objetos conocidos](example-code-for-binding-to-well-known-objects.md).

 

 