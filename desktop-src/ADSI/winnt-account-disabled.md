---
title: Cuenta deshabilitada (proveedor winNT)
description: Cuando se usa el proveedor WinNT, se puede habilitar o deshabilitar una cuenta mediante la propiedad IADsUser.AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Cuenta deshabilitada (proveedor winNT)
- ADSI deshabilitado de cuenta, proveedor winNT
- ADSI del proveedor winNT, ejemplos de administración de usuarios, cuenta deshabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1659bad4ab930615aed7d02e3c54fc3899b60eb476999676ff765fe2a2e94f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178510"
---
# <a name="account-disabled-winnt-provider"></a>Cuenta deshabilitada (proveedor winNT)

Cuando se usa el proveedor WinNT, una cuenta se puede habilitar o deshabilitar mediante la [**propiedad IADsUser.AccountDisabled.**](iadsuser-property-methods.md)

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta Visual Basic con ADSI.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta mediante C++ con ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




