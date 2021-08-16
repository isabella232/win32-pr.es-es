---
title: Método Get
description: El método Get de los IAD se usa para recuperar atributos con nombre individuales de un objeto de directorio.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Obtener ADSI mediante IAD Get
- ADSI ADSI , mediante, mediante el método Get de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386c3fe6e50a9f7357ec161b1e6bd8731cf8d0a74eed4b4a765adc3315c1045d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838635"
---
# <a name="the-get-method"></a>Método Get

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



En los lenguajes de Automation, también se puede acceder directamente a los atributos con nombre mediante la notación de puntos. Por ejemplo, **object. Get("distinguishedName") es** idéntico a **object.distinguishedName.**

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

 

 




