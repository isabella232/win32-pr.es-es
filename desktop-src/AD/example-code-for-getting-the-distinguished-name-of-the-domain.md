---
title: Código de ejemplo para obtener el nombre distintivo del dominio
description: En este tema se incluye un ejemplo de código que obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, obtener el nombre distintivo del dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268285"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Código de ejemplo para obtener el nombre distintivo del dominio

En este tema se incluye un ejemplo de código que obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.

En el siguiente ejemplo de código de Visual Basic se obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



En el siguiente ejemplo de código de C# se obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



El siguiente ejemplo de código de C/C++ obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




