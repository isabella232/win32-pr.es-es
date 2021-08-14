---
title: Modificar el usuario no puede cambiar la contraseña (proveedor winNT)
description: Obtenga información sobre cómo denegar a un usuario el permiso para cambiar una contraseña para el proveedor winNT. Se puede conceder o denegar la capacidad de un usuario para cambiar su propia contraseña.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Modificar el usuario no puede cambiar la contraseña (proveedor winNT)
- El usuario no puede cambiar la contraseña (proveedor winNT), modificar
- ADSI del proveedor WinNT, ejemplos de administración de usuarios,Usuario no puede cambiar contraseña, modificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b510fb08172a178a454ee731110765844368ca78108047a7a5a738b78b6a196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178969"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a>Modificar el usuario no puede cambiar la contraseña (proveedor winNT)

La capacidad de un usuario para cambiar su propia contraseña es un permiso que se puede conceder o denegar. Para denegar este permiso, agregue la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** a la **propiedad userFlags** del objeto de usuario. Para conceder este permiso, quite la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la **propiedad userFlags** del objeto de usuario.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra cómo cambiar la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la **propiedad userFlags** de un objeto de usuario.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



En el ejemplo de código siguiente se muestra cómo cambiar la marca **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** de la **propiedad userFlags** de un objeto de usuario.


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




