---
title: Código de ejemplo para obtener el nombre distintivo del dominio
description: En este tema se incluye un ejemplo de código que obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , obtención del nombre distintivo del dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693649"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Código de ejemplo para obtener el nombre distintivo del dominio

En este tema se incluye un ejemplo de código que obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.

En el Visual Basic ejemplo de código siguiente se obtiene el nombre distintivo del dominio del que es miembro el equipo local mediante el enlace sin servidor.


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



 

 




