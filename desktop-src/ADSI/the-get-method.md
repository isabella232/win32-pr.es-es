---
title: El método get
description: El método get de IADs se utiliza para recuperar los atributos con nombre individuales de un objeto de directorio.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Obtener ADSI mediante IADs Get
- ADSI ADSI, usar, usar el método get de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656142"
---
# <a name="the-get-method"></a>El método get

El método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) se utiliza para recuperar los atributos con nombre individuales de un objeto de directorio.

En el ejemplo de código siguiente se usa el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar un atributo con nombre de un objeto.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



En los lenguajes de automatización, también se puede tener acceso a los atributos con nombre directamente mediante la notación de puntos. Por ejemplo, **objeto. Get ("distinguishedName")** es idéntico a **Object. distinguishedName**.

El siguiente ejemplo de código es idéntico al ejemplo anterior, salvo que se tiene acceso al atributo **distinguishedName** mediante la notación de puntos.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Si no se establece un valor en el objeto, el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) devolverá el error "propiedad no encontrada en la memoria caché".

 

 




