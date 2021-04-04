---
title: Usar objectGUID para enlazar a un objeto
description: Un nombre distintivo de objeto cambia si se cambia el nombre o se mueve el objeto, por lo que el nombre distintivo no es un identificador de objeto confiable.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Usar objectGUID para enlazar a un objeto AD
- TITULAR de objectGUID
- objectGUID AD, usar para enlazar a un objeto
- Active Directory, usar, enlazar, usar objectGUID para enlazar a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077485"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Usar objectGUID para enlazar a un objeto

Un nombre distintivo de objeto cambia si se cambia el nombre o se mueve el objeto, por lo que el nombre distintivo no es un identificador de objeto confiable. En Active Directory Domain Services, la propiedad **objectGUID** de un objeto nunca cambia, aunque se cambie el nombre del objeto o se mueva. Para obtener más información sobre **objectGUID** e identificadores, vea [nombres de objeto e identidades](object-names-and-identities.md).

El proveedor LDAP Active Directory proporciona un método para enlazar a un objeto utilizando el GUID del objeto. El formato de la cadena de enlace es el siguiente:


```C++
LDAP://servername/<GUID=XXXXX>
```



En este ejemplo, "ServerName" es el nombre del servidor de directorio y "XXXXX" es la representación de cadena del valor hexadecimal del GUID. "ServerName" es opcional. La cadena GUID se especifica en el formulario "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX". La cadena GUID también puede tener la forma "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", que es la misma forma que la cadena generada por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sin las llaves circundantes " {} ". Para obtener más información y un ejemplo de código que muestra cómo crear una cadena enlazable desde un GUID, vea el [código de ejemplo para crear una representación de cadena enlazable de un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). La propiedad [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) se puede usar para recuperar el formato de cadena correcto del GUID.

Al enlazar con el GUID del objeto, no se admiten algunos métodos y propiedades de [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Las siguientes propiedades de **IADs** no son compatibles con los objetos obtenidos mediante el enlace con el GUID del objeto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nombre**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Los métodos **IADsContainer** siguientes no son compatibles con los objetos obtenidos mediante el enlace con el GUID del objeto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**A**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Elimínelos**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Para usar estos métodos y propiedades después de enlazar a un objeto mediante el GUID del objeto, use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el nombre distintivo del objeto y, a continuación, use el nombre distintivo para enlazarlo de nuevo al objeto.

Si una aplicación almacena o almacena en caché identificadores o referencias a objetos almacenados en Active Directory Domain Services, el GUID del objeto es el mejor identificador que se debe usar por varias razones:

-   La propiedad **objectGUID** de en el objeto nunca cambia aunque se cambie el nombre del objeto o se mueva.
-   Es fácil enlazar con el objeto mediante el GUID del objeto.
-   Si se cambia el nombre del objeto o se mueve, la propiedad **objectGUID** proporciona un identificador único que se puede usar para buscar e identificar rápidamente el objeto en lugar de tener que crear una consulta que tenga condiciones para todas las propiedades que identifiquen ese objeto.

 

 