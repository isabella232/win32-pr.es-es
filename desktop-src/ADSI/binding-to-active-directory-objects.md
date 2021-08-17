---
title: Enlace a Active Directory objetos
description: Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos. Enlazar un objeto ADSI conecta el objeto con el servicio de directorio y permite acceder a los métodos del objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b473c9e3370c3d1739fc904b8c6409d756f62b5c358db200c3de821f55349f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962264"
---
# <a name="binding-to-active-directory-objects"></a>Enlace a Active Directory objetos

Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos. Enlazar un objeto ADSI conecta el objeto con el servicio de directorio y permite acceder a los métodos del objeto.

## <a name="adspath"></a>ADsPath

Un objeto ADSI se identifica de forma única mediante su cadena de enlace, que también se conoce como ADsPath. ADsPath es una combinación de un identificador de programación (progID) del proveedor ADSI y el nombre distintivo (DN) del objeto.

Este es el formato de ADsPath:

"progID://DN"

-   pogID: identificador mediante programación del proveedor adsi, como LDAP o WinNT.

-   :// : separa el progID del DN.

-   DN: nombre distintivo del objeto ADSI, que es la ruta de acceso completa del objeto, donde la ruta de acceso consta de nombres distintivos relativos (RDN).

Un RDN es el nombre del objeto sin la ruta de acceso y es único de sus objetos relacionados. Un RDN consta de un identificador de atributo y un valor, como "DC=Fabrikam", donde DC es el atributo y Fabrikam es el valor. DC es un identificador de atributo RDN que significa componente de dominio.

Este es un ejemplo de ADsPath:

"LDAP://DC=Fabrikam,DC=Com"

## <a name="binding-the-object"></a>Enlazar el objeto

Aquí se muestra cómo puede enlazar el objeto de dominio en este escenario:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Al ejecutar este ejemplo de código, ADSI usa el DN para determinar los objetos ADSI que se enlazarán. Una vez que ADSI enlaza estos objetos, puede acceder a sus métodos. En el ejemplo de código anterior se enlaza un objeto de dominio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Ahora puede usar métodos en esas interfaces, como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put,**](/windows/desktop/api/Iads/nf-iads-iads-put) [**Create,**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)y [**MoveHere.**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)

Después de enlazar un objeto de dominio, puede imprimir algunos de sus atributos:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Para obtener más información sobre ADsPath, vea [Binding String](binding-string.md). Para obtener más información sobre el enlace, vea [Enlace a un objeto ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una unidad organizativa](creating-an-organizational-unit.md)
</dt> </dl>

 

 




