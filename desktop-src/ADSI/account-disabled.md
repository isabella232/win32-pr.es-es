---
title: Cuenta deshabilitada (proveedor LDAP)
description: Para deshabilitar una cuenta de usuario, establezca la propiedad AccountDisabled en TRUE en la interfaz IADsUser. Esto es similar al proveedor de Winnt. En los siguientes ejemplos de código se muestra cómo deshabilitar una cuenta de usuario.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Cuenta ADSI deshabilitada, proveedor LDAP
- ADSI Provider LDAP, ejemplos de administración de usuarios, cuenta deshabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660097"
---
# <a name="account-disabled-ldap-provider"></a>Cuenta deshabilitada (proveedor LDAP)

Para deshabilitar una cuenta de usuario, establezca la propiedad AccountDisabled en **true** en la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . Esto es similar al proveedor de Winnt. En los siguientes ejemplos de código se muestra cómo deshabilitar una cuenta de usuario.

## <a name="example-1"></a>Ejemplo 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>Ejemplo 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




