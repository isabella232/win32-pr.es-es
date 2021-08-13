---
title: Método GetEx
description: Algunos atributos pueden almacenar uno o varios valores.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, mediante IAD GetEx
- ADSI ADSI , mediante, mediante el método GetEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e656bd6a48830feb725e927f08be1d573e7b0232cf02c16ee87bd7d6a5b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690154"
---
# <a name="the-getex-method"></a>Método GetEx

Algunos atributos pueden almacenar uno o varios valores. Por ejemplo, el **atributo otherTelephone** de un objeto de usuario en Active Directory es una propiedad que puede tener cero, uno o varios valores. Los atributos que tienen varios valores se conocen como "atributos multivalor". Si se usa el método [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar un atributo con varios valores, los resultados se deben procesar de forma diferente a si el atributo tiene un único valor. Sin embargo, los resultados proporcionados por el método [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) se procesan de la misma manera, independientemente de si el atributo tiene uno o varios valores. En ambos casos, **el método IADs::GetEx** devuelve los valores de una matriz.

El [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera propiedades de la caché de propiedades. Si la propiedad especificada no se encuentra en la memoria caché, **IADs::GetEx** realiza una llamada [**implícita a IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)

El [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve una matriz variante de variantes independientemente del número de valores devueltos por el servidor. Esto es cierto incluso si el atributo solo contiene un valor.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



El [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) también se puede usar para atributos con un solo valor. Los resultados de un atributo con un solo valor se procesan igual que los resultados de un atributo con varios valores.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Si no se establece ningún valor para el atributo , [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve el error "Property not found in cache".

 

 




