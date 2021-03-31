---
title: Traslado de usuarios existentes a la unidad organizativa
description: Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4,0 a Active Directory, se migran todos los usuarios y grupos a los contenedores de usuarios del dominio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Traslado de usuarios existentes a la unidad organizativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268256"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Traslado de usuarios existentes a la unidad organizativa

Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4,0 a Active Directory, se migran todos los usuarios y grupos a los contenedores de usuarios del dominio fabrikam. Joe ahora puede trasladar esos usuarios y grupos a las unidades organizativas adecuadas. También se puede desplazar un objeto entre dominios de Windows 2000 relacionados mediante ADSI.

En el ejemplo de código siguiente, Joe mueve "juanpérez" a la organización de ventas.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



El método [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) toma el ADsPath del objeto que se va a desplace y el nuevo nombre de objeto (RDN). Para mantener el mismo nombre, puede especificar **null** (**vbNullString**) para el parámetro *bstrNewName* . Para cambiar el nombre del objeto cuando se mueve, especifique el nuevo nombre distintivo relativo para el parámetro *bstrNewName* . Por ejemplo, para migrar juanpérez a la organización sales y cambiar el nombre del objeto "juanpérez" a "Jeff \_ Smith" en la misma operación, Joe ejecutaría el código siguiente:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de nuevos usuarios en la unidad organizativa](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




