---
title: Creación de nuevos usuarios en la unidad organizativa
description: Tomás Adams se contrató en la organización de ventas de fabrikam. Su informe directo es Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creación de nuevos usuarios en la unidad organizativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486566"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Creación de nuevos usuarios en la unidad organizativa

Tomás Adams se contrató en la organización de ventas de fabrikam. Su informe directo es Patrick Hines.

Como se muestra en el ejemplo de código siguiente, Joe Andreshak, el administrador de la empresa, creará una nueva cuenta para él.


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



Al crear un nuevo usuario, debe especificar un **samAccountName**. Este es un atributo obligatorio para la clase User. Antes de que se pueda crear una instancia de un objeto, se deben establecer todos los atributos obligatorios. El **samAccountName** se generará automáticamente si no se especifica uno para un nuevo usuario.

Al crear un nuevo usuario, todos los atributos necesarios se deben establecer en la memoria caché local antes de que se llame al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Joe, como administrador, puede asignar la contraseña de Tomás mediante el método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) . El método **IADsUser. SetPassword** no funcionará hasta que se haya llamado al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

A continuación, Joe habilita la cuenta de usuario estableciendo la propiedad [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) en **false**.

En el ejemplo de código siguiente se muestra cómo establecer Tomás como administrador de Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Es posible que se pregunte qué sucede si Terry cambia su nombre, se desplaza a otra organización o deja la empresa. ¿Quién mantiene este vínculo de informe de administrador-directo? Para obtener más información y la solución a este problema, vea [reorganización](reorganization.md). Dado que el esquema de Active Directory es extensible, puede modelar los objetos para que incluyan relaciones similares de estilo de informe directo entre administradores.

Antes de pasar a la tarea siguiente, consulte un ejemplo de código que muestra cómo Joe vería los informes directos de Terry.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



En este ejemplo de código, Patrick se mostrará como el informe directo de Terry, aunque el atributo **directReports** no se haya modificado nunca. Active Directory lo hace automáticamente.

En el mundo del directorio, un atributo puede tener uno o varios valores. Dado que **directReports** tiene varios valores, puede obtener esta información examinando el esquema, es más fácil usar el método [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , que devuelve una matriz de valores independientemente de si se devuelve uno o varios valores.

El complemento usuarios y equipos de Active Directory permite ver informes directos y relaciones de administrador en la página de propiedades del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar usuarios a un grupo](adding-users-to-a-group.md)
</dt> </dl>

 

 




