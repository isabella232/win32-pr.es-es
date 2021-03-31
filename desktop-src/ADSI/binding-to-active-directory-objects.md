---
title: Enlazar a objetos de Active Directory
description: Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos. El enlace de un objeto ADSI conecta el objeto con el servicio de directorio y permite tener acceso a los métodos del objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075081"
---
# <a name="binding-to-active-directory-objects"></a>Enlazar a objetos de Active Directory

Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos. El enlace de un objeto ADSI conecta el objeto con el servicio de directorio y permite tener acceso a los métodos del objeto.

## <a name="adspath"></a>ADsPath

Un objeto ADSI se identifica de forma única mediante su cadena de enlace, que también se conoce como ADsPath. ADsPath es una combinación de un identificador de programación (progID) del proveedor ADSI y el nombre distintivo (DN) del objeto.

Este es el formato de ADsPath:

"progID://DN"

-   pogID: el identificador de programación del proveedor ADSI, como LDAP o Winnt.

-   ://: separa el progID del DN.

-   DN: nombre distintivo del objeto ADSI, que es la ruta de acceso completa del objeto, donde la ruta de acceso consta de nombres distintivos relativos (RDN).

Un RDN es el nombre del objeto sin la ruta de acceso y es único de sus objetos relacionados. Un RDN consta de un identificador de atributo y un valor, como "DC = Fabrikam", donde DC es el atributo y Fabrikam es el valor. DC es un identificador de atributo RDN que representa el componente de dominio.

A continuación se muestra un ejemplo de una ADsPath:

"LDAP://DC = Fabrikam, DC = com"

## <a name="binding-the-object"></a>Enlazar el objeto

A continuación se muestra cómo puede enlazar el objeto de dominio en este escenario:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Al ejecutar este ejemplo de código, ADSI utiliza el DN para determinar los objetos ADSI que se van a enlazar. Una vez que ADSI enlaza estos objetos, puede tener acceso a sus métodos. En el ejemplo de código anterior se enlaza un objeto de dominio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Ahora puede usar métodos en esas interfaces como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)y [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Después de enlazar un objeto de dominio, puede imprimir algunos de sus atributos:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Para obtener más información sobre ADsPath, consulte [cadena de enlace](binding-string.md). Para obtener más información sobre el enlace, vea [enlazar a un objeto ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una unidad organizativa](creating-an-organizational-unit.md)
</dt> </dl>

 

 




