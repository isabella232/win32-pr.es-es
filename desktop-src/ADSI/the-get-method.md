---
title: El método Get
description: El método Get de IADs se usa para recuperar atributos con nombre individuales de un objeto de directorio.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Obtener ADSI mediante los IAD Get
- ADSI ADSI , using,using the IADs Get (Método Get de IADs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172185"
---
# <a name="the-get-method"></a>El método Get

El [**método IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) se usa para recuperar atributos con nombre individuales de un objeto de directorio.

En el ejemplo de código siguiente se usa [**el método IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar un atributo con nombre de un objeto .


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



En los lenguajes de Automation, también se puede acceder a los atributos con nombre directamente mediante la notación de puntos. Por ejemplo, **object. Get("distinguishedName") es** idéntico a **object.distinguishedName.**

El ejemplo de código siguiente es idéntico al ejemplo anterior, salvo que se tiene acceso al atributo **distinguishedName** mediante la notación de puntos.


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



Si no se establece un valor en el objeto , el método [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) devolverá el error "Property not found in cache".

 

 




