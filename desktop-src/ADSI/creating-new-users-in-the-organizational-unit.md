---
title: Creación de nuevos usuarios en la unidad organizativa
description: Adams se conscribía en la organización Fabrikam Sales. Su informe directo es Patrick Hincapiés.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creación de nuevos usuarios en el ADSI de la unidad organizativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76d62c8d95e7d5e421fc562e38716477ff2dfb8f4097d4652710e2c50715487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180120"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Creación de nuevos usuarios en la unidad organizativa

Adams se conscribía en la organización Fabrikam Sales. Su informe directo es Patrick Hincapiés.

Como se muestra en el ejemplo de código siguiente, Joe Andreshak, el administrador de la empresa, creará una cuenta para él.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



Al crear un nuevo usuario, debe especificar **sAMAccountName**. Se trata de un atributo obligatorio para la clase de usuario. Para poder crear una instancia de un objeto, se deben establecer todos los atributos obligatorios. **SAMAccountName** se generará automáticamente si no se especifica uno para un nuevo usuario.

Al crear un nuevo usuario, todos los atributos necesarios deben establecerse en la memoria caché local antes de llamar al método [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

Joe, como administrador, puede asignar la contraseña de Joe mediante el [**método IADsUser.SetPassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) El **método IADsUser.SetPassword** no funcionará hasta que se llame al método [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

A continuación, Joe habilita la cuenta de usuario estableciendo la propiedad [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) en **FALSE.**

En el ejemplo de código siguiente se muestra cómo establecer a Patrick como administrador de Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Es posible que se pregunte qué ocurre si Cambia su nombre, se mueve a otra organización o deja la empresa. Quién mantiene este vínculo de informe directo del administrador? Para obtener más información y la solución a este problema, vea [Reorganización](reorganization.md). Dado que Active Directory esquema es extensible, puede modelar los objetos para incluir relaciones similares de estilo de informe directo del administrador.

Antes de pasar a la siguiente tarea, vea un ejemplo de código que muestra cómo Vería Joe los informes directos de Joe.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



En este ejemplo de código, Patrick se mostrará como informe directo de Patrick, aunque el **atributo directReports** nunca se modificó. Active Directory hace esto automáticamente.

En el mundo de los directorios, un atributo puede tener uno o varios valores. Dado **que directReports** tiene varios valores, puede obtener esta información consultando el esquema, es más fácil usar el método [**IADs.GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) que devuelve una matriz de valores independientemente de si se devuelven uno o varios valores.

El Usuarios y equipos de Active Directory complemento permite ver informes directos y relaciones de administrador en la página de propiedades del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar usuarios a un grupo](adding-users-to-a-group.md)
</dt> </dl>

 

 




