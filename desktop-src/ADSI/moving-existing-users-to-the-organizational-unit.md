---
title: Mover usuarios existentes a la unidad organizativa
description: Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4.0 a Active Directory, todos los usuarios y grupos se migran a los contenedores Usuarios del dominio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Traslado de usuarios existentes a la unidad organizativa de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178959"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Mover usuarios existentes a la unidad organizativa

Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4.0 a Active Directory, todos los usuarios y grupos se migran a los contenedores Usuarios del dominio fabrikam. Joe ahora puede mover esos usuarios y grupos a las unidades organizativas adecuadas. Un objeto también se puede mover entre dominios Windows 2000 mediante ADSI.

En el ejemplo de código siguiente, Joe mueve "jeffsmith" a la organización Sales.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



El [**método IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) toma el ADsPath del objeto que se va a mover y el nuevo nombre de objeto (RDN). Para mantener el mismo nombre, puede especificar **NULL** (**vbNullString**) para el *parámetro bstrNewName.* Para cambiar el nombre del objeto cuando se mueve, especifique el nuevo nombre distintivo relativo para el *parámetro bstrNewName.* Por ejemplo, para mover jeffsmith a la organización de ventas y cambiar el nombre del objeto "jeffsmith" a "jeff smith" en la misma \_ operación, Joe ejecutaría el código siguiente:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de nuevos usuarios en la unidad organizativa](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




