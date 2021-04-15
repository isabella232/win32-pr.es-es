---
title: El método GetEx
description: Algunos atributos pueden almacenar uno o más valores.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, usar GetEx de IADs
- ADSI ADSI, usar, usar el método GetEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656141"
---
# <a name="the-getex-method"></a>El método GetEx

Algunos atributos pueden almacenar uno o más valores. Por ejemplo, el atributo **otherTelephone** de un objeto de usuario en Active Directory es una propiedad que puede tener cero, uno o varios valores. Los atributos que tienen varios valores se conocen como "atributos multivalor". Si el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) se usa para recuperar un atributo con varios valores, los resultados se deben procesar de forma diferente que si el atributo tiene un valor único. Los resultados proporcionados por el método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , sin embargo, se procesan de la misma manera, independientemente de si el atributo tiene uno o varios valores. En ambos casos, el método **IADs:: GETEX** devuelve los valores de una matriz.

El método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera propiedades de la memoria caché de propiedades. Si la propiedad especificada no se encuentra en la memoria caché, **IADs:: GETEX** realiza una llamada a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita.

El método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve una matriz de variantes variante sin tener en consideración el número de valores devueltos por el servidor. Esto es así incluso si el atributo solo contiene un valor.


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



También se puede usar el método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) para los atributos de valor único. Los resultados de un atributo de un solo valor se procesan de la misma forma que los resultados de un atributo con varios valores.


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



Si no se establece ningún valor para el atributo, [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve el error "propiedad no encontrada en la memoria caché".

 

 




