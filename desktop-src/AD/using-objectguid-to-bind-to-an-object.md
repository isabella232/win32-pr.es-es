---
title: Usar objectGUID para enlazar a un objeto
description: Un nombre distintivo de objeto cambia si se cambia el nombre del objeto o se mueve, por lo que el nombre distintivo no es un identificador de objeto confiable.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Uso de objectGUID para enlazar a un ad de objeto
- objectGUID AD
- objectGUID AD , mediante para enlazar a un objeto
- Active Directory, mediante, enlazar, usar objectGUID para enlazar al objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c310ad1041c072dc126a761fab5fa104fa00c4f98e4fa01d45ca7bc24c11b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024493"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Usar objectGUID para enlazar a un objeto

Un nombre distintivo de objeto cambia si se cambia el nombre del objeto o se mueve, por lo que el nombre distintivo no es un identificador de objeto confiable. En Active Directory Domain Services, la propiedad **objectGUID de** un objeto nunca cambia, incluso si se cambia el nombre del objeto o se mueve. Para obtener más información sobre **objectGUID** e identificadores, vea [Nombres de objeto e identidades.](object-names-and-identities.md)

El Active Directory LDAP proporciona un método para enlazar a un objeto mediante el GUID del objeto. El formato de cadena de enlace es el siguiente:


```C++
LDAP://servername/<GUID=XXXXX>
```



En este ejemplo, "servername" es el nombre del servidor de directorio y "XXXXX" es la representación de cadena del valor hexadecimal del GUID. "servername" es opcional. La cadena GUID se especifica en el formulario "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX". La cadena GUID también puede tener la forma "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", que es la misma forma que la cadena producida por la función [**StringFromGUID2,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) sin las llaves circundantes " {} ". Para obtener más información y un ejemplo de código que muestra cómo crear una cadena enlazable a partir de un GUID, vea Código de ejemplo para crear una representación de cadena enlazable [de un GUID.](example-code-for-creating-a-bindable-string-representation-of-a-guid.md) La [**propiedad IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) se puede usar para recuperar el formato de cadena adecuado del GUID.

Al enlazar mediante el GUID del objeto, [**no**](/windows/desktop/api/iads/nn-iads-iads) se admiten algunos identificadores y propiedades [**de IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer) Los objetos **obtenidos** mediante el enlace no admiten las siguientes propiedades de identificador mediante el GUID del objeto:

-   [**Adspath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nombre**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Los siguientes **métodos IADsContainer** no son compatibles con los objetos obtenidos mediante el enlace mediante el GUID del objeto:

-   [**Getobject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Crear**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Eliminar**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Para usar estos métodos y propiedades después de enlazar a un objeto mediante el GUID del objeto, use el método [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el nombre distintivo del objeto y, a continuación, use el nombre distintivo para enlazar de nuevo al objeto.

Si una aplicación almacena o almacena en caché identificadores o referencias a objetos almacenados en Active Directory Domain Services, el GUID del objeto es el mejor identificador que se puede usar por varias razones:

-   La **propiedad objectGUID** de en el objeto nunca cambia incluso si se cambia el nombre del objeto o se mueve.
-   Es fácil enlazar al objeto mediante el GUID del objeto.
-   Si se cambia el nombre del objeto o se mueve, la propiedad **objectGUID** proporciona un identificador único que se puede usar para buscar e identificar rápidamente el objeto en lugar de tener que crear una consulta que tenga condiciones para todas las propiedades que identificarían ese objeto.

 

 