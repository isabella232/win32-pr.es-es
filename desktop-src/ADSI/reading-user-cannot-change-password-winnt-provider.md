---
title: Leer que el usuario no puede cambiar la contraseña (proveedor winNT)
description: Obtenga información sobre cómo determinar si un usuario tiene permiso para cambiar una contraseña para el proveedor winNT. La capacidad de un usuario para cambiar una contraseña se puede conceder o denegar.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- LEER ADSI del usuario no puede cambiar la contraseña (proveedor winNT)
- El usuario no puede cambiar la contraseña (proveedor winNT) ADSI , lectura
- ADSI del proveedor WinNT, ejemplos de administración de usuarios,Usuario no puede cambiar contraseña, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246981"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Leer que el usuario no puede cambiar la contraseña (proveedor winNT)

La capacidad de un usuario para cambiar su propia contraseña es un permiso que se puede conceder o denegar. Para determinar si se ha concedido este permiso al usuario con el proveedor winNT, lea la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la propiedad **userFlags** del objeto de usuario. La **marca ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** se define en la [**\_ enumeración \_ \_ ENUM USER FLAG de ADS.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)

## <a name="example-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra cómo obtener la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la **propiedad userFlags** de un objeto de usuario.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



En el ejemplo de código siguiente se muestra cómo obtener la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la **propiedad userFlags** de un objeto de usuario.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




