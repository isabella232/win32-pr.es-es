---
title: Bloqueo de cuenta (proveedor de WinNT)
description: Cuando se supera el número de intentos de inicio de sesión erróneos, la cuenta de usuario se bloquea durante el número de minutos especificado por el atributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Bloqueo de cuenta ADSI, proveedor de Winnt
- ADSI del proveedor de WinNT, ejemplos de administración de usuarios, bloqueo de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656411"
---
# <a name="account-lockout-winnt-provider"></a>Bloqueo de cuenta (proveedor de WinNT)

Cuando se supera el número de intentos de inicio de sesión erróneos, la cuenta de usuario se bloquea durante el número de minutos especificado por el atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . La propiedad [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser la propiedad que se va a usar para leer y modificar el estado de bloqueo de una cuenta de usuario, pero el proveedor ADSI de WinNT tiene restricciones que limitan el uso de la propiedad **IsAccountLocked** .

## <a name="resetting-the-account-lockout-status"></a>Restableciendo el estado de bloqueo de cuenta

Cuando se usa el proveedor de WinNT, la propiedad [**IsAccountLocked**](iadsuser-property-methods.md) solo se puede establecer en **false**, lo que desbloquea la cuenta. Se producirá un error al intentar establecer la propiedad **IsAccountLocked** en **true** . Solo el sistema puede bloquear una cuenta.

En el ejemplo de código siguiente se muestra cómo usar Visual Basic con ADSI para desbloquear una cuenta de usuario.


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



En el ejemplo de código siguiente se muestra cómo utilizar C++ con ADSI para desbloquear una cuenta de usuario.


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



## <a name="reading-the-account-lockout-status"></a>Leer el estado de bloqueo de cuenta

Con el proveedor de WinNT, la propiedad [**IsAccountLocked**](iadsuser-property-methods.md) se puede usar para determinar si una cuenta está bloqueada. Si una cuenta está bloqueada, la propiedad **IsAccountLocked** contendrá **true**. Si una cuenta no está bloqueada, la propiedad **IsAccountLocked** contendrá **false**.

En el ejemplo de código siguiente se muestra cómo usar Visual Basic con ADSI para determinar si una cuenta está bloqueada.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



En el ejemplo de código siguiente se muestra cómo utilizar C++ con ADSI para determinar si una cuenta está bloqueada.


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



 

 