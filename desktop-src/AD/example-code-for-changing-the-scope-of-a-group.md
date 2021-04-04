---
title: Código de ejemplo para cambiar el ámbito de un grupo
description: Este tema contiene código de ejemplo para cambiar el ámbito de un grupo.
ms.assetid: 4ae61101-f123-44bd-8bec-bade51d22217
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, cambiar el ámbito de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641ad43604785a6aae5bb250061ff0a3b62c294e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075134"
---
# <a name="example-code-for-changing-the-scope-of-a-group"></a>Código de ejemplo para cambiar el ámbito de un grupo

En el siguiente ejemplo de código de C++ se cambia el ámbito de un grupo.


```C++

    WCHAR *pwszLDAPPath = 
        L"LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com";
 
    HRESULT hr;
    IADsGroup * pGroup = NULL;
 
    // Initialize COM.
    CoInitialize(0);
 
    // Bind to the passed container. 
    hr = ADsGetObject( pwszLDAPPath, IID_IADsGroup,(void **)&pGroup);
 
    if (SUCCEEDED(hr))
    {
        VARIANT vValue;
        BSTR    bsValue = SysAllocString(L"groupType");
        VariantInit(&vValue);
    // Set a new GroupType Value.
        vValue.vt = VT_I4;
        vValue.lVal = ADS_GROUP_TYPE_GLOBAL_GROUP ;
 
        hr = pGroup->Put(bsValue,vValue);
        hr = pGroup->SetInfo();
        pGroup->Release();
        pGroup= NULL;
        SysFreeString(bsValue);
    }
 
    CoUninitialize();
```



En el siguiente ejemplo de código Visual Basic se cambia el ámbito de un grupo.


```VB
Dim x as IADs
On Error GoTo CleanUp
Set x = GetObject("LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com")
x.Put "groupType", 
    ADS_GROUP_TYPE_UNIVERSAL_GROUP|ADS_GROUP_TYPE_SECURITY_ENABLED
Exit Sub

CleanUp:
    MsgBox("An error has occurred.")
    x = Nothing
```



 

 




