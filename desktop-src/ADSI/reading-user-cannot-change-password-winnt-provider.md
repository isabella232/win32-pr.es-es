---
title: Lectura de usuario no puede cambiar la contraseña (proveedor WinNT)
description: La capacidad de un usuario de cambiar su propia contraseña es un permiso que se puede conceder o denegar.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Leer usuario no puede cambiar la contraseña (proveedor WinNT) ADSI
- El usuario no puede cambiar la contraseña (proveedor WinNT) ADSI, leer
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, el usuario no puede cambiar la contraseña, leer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab257f620d3e103866639f8ecacb57cc924efec4
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "103994991"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Lectura de usuario no puede cambiar la contraseña (proveedor WinNT)

La capacidad de un usuario de cambiar su propia contraseña es un permiso que se puede conceder o denegar. Para determinar si el usuario ha concedido este permiso con el proveedor de WinNT, lea la marca de modificación de la etiqueta de cambio no se pudo **\_ \_ \_ \_ cambiar** de la propiedad **userFlags** del objeto de usuario. La marca de cambio de no se pudo **\_ \_ \_ \_ cambiar** la etiqueta [**de \_ usuario \_ \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) de ad

## <a name="example-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra cómo obtener la marca de  cambio de la propiedad de la propiedad userFlags de un objeto de usuario de **ADS \_ up \_ passwd \_ \_** .


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



En el ejemplo de código siguiente se muestra cómo obtener la marca de  cambio de la propiedad de la propiedad userFlags de un objeto de usuario de **ADS \_ up \_ passwd \_ \_** .


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



 

 




