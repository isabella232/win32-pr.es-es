---
title: Bloqueo de cuenta (proveedor WinNT)
description: Cuando se supera el número de intentos de inicio de sesión con error, la cuenta de usuario se bloquea durante el número de minutos especificado por el atributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- ADSI de bloqueo de cuenta, proveedor WinNT
- ADSI del proveedor WinNT, ejemplos de administración de usuarios, bloqueo de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e28c2a4bf58f5559070af78ca55235e8b10c16b2b856a63a256767d4d67a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838365"
---
# <a name="account-lockout-winnt-provider"></a>Bloqueo de cuenta (proveedor WinNT)

Cuando se supera el número de intentos de inicio de sesión con error, la cuenta de usuario se bloquea durante el número de minutos especificado por [**el atributo lockoutDuration.**](/windows/desktop/ADSchema/a-lockoutduration) La propiedad [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) parece ser la propiedad que se va a usar para leer y modificar el estado de bloqueo de una cuenta de usuario, pero el proveedor ADSI de WinNT tiene restricciones que limitan el uso de la **propiedad IsAccountLocked.**

## <a name="resetting-the-account-lockout-status"></a>Restablecer el estado de bloqueo de la cuenta

Cuando se usa el proveedor WinNT, la [**propiedad IsAccountLocked**](iadsuser-property-methods.md) solo se puede establecer en **FALSE,** lo que desbloquea la cuenta. Se producirá un error al intentar establecer **la propiedad IsAccountLocked** en **TRUE.** Solo el sistema puede bloquear una cuenta.

En el ejemplo de código siguiente se muestra cómo usar Visual Basic adsi para desbloquear una cuenta de usuario.


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



En el ejemplo de código siguiente se muestra cómo usar C++ con ADSI para desbloquear una cuenta de usuario.


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>Leer el estado de bloqueo de la cuenta

Con el proveedor WinNT, se puede usar [**la propiedad IsAccountLocked**](iadsuser-property-methods.md) para determinar si una cuenta está bloqueada. Si una cuenta está bloqueada, la **propiedad IsAccountLocked** contendrá **TRUE.** Si una cuenta no está bloqueada, la **propiedad IsAccountLocked** contendrá **FALSE.**

En el ejemplo de código siguiente se muestra cómo usar Visual Basic adsi para determinar si una cuenta está bloqueada.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



En el ejemplo de código siguiente se muestra cómo usar C++ con ADSI para determinar si una cuenta está bloqueada.


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 