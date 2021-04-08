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
# <a name="reading-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="786c7-106">Lectura de usuario no puede cambiar la contraseña (proveedor WinNT)</span><span class="sxs-lookup"><span data-stu-id="786c7-106">Reading User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="786c7-107">La capacidad de un usuario de cambiar su propia contraseña es un permiso que se puede conceder o denegar.</span><span class="sxs-lookup"><span data-stu-id="786c7-107">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="786c7-108">Para determinar si el usuario ha concedido este permiso con el proveedor de WinNT, lea la marca de modificación de la etiqueta de cambio no se pudo **\_ \_ \_ \_ cambiar** de la propiedad **userFlags** del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="786c7-108">To determine if the user has been granted this permission with the WinNT provider, read the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of the user object.</span></span> <span data-ttu-id="786c7-109">La marca de cambio de no se pudo **\_ \_ \_ \_ cambiar** la etiqueta [**de \_ usuario \_ \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) de ad</span><span class="sxs-lookup"><span data-stu-id="786c7-109">The **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag is defined in the [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) enumeration.</span></span>

## <a name="example-code"></a><span data-ttu-id="786c7-110">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="786c7-110">Example Code</span></span>

<span data-ttu-id="786c7-111">En el ejemplo de código siguiente se muestra cómo obtener la marca de  cambio de la propiedad de la propiedad userFlags de un objeto de usuario de **ADS \_ up \_ passwd \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="786c7-111">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



<span data-ttu-id="786c7-112">En el ejemplo de código siguiente se muestra cómo obtener la marca de  cambio de la propiedad de la propiedad userFlags de un objeto de usuario de **ADS \_ up \_ passwd \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="786c7-112">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



 

 




