---
title: El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor LDAP)
description: Para obligar a un usuario a cambiar su contraseña en el siguiente inicio de sesión, establezca el atributo pwdLastSet en cero (0). Para quitar este requisito, establezca el atributo pwdLastSet en-1. El atributo pwdLastSet no se puede establecer en ningún otro valor excepto en el sistema.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- El usuario debe cambiar la contraseña en el siguiente inicio de sesión ADSI, proveedor LDAP
- ADSI Provider LDAP, ejemplos de administración de usuarios, el usuario debe cambiar la contraseña en el siguiente inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075056"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a><span data-ttu-id="aaf97-107">El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="aaf97-107">User Must Change Password at Next Logon (LDAP Provider)</span></span>

<span data-ttu-id="aaf97-108">Para obligar a un usuario a cambiar su contraseña en el siguiente inicio de sesión, establezca el atributo **pwdLastSet** en cero (0).</span><span class="sxs-lookup"><span data-stu-id="aaf97-108">To force a user to change their password at next logon, set the **pwdLastSet** attribute to zero (0).</span></span> <span data-ttu-id="aaf97-109">Para quitar este requisito, establezca el atributo **pwdLastSet** en-1.</span><span class="sxs-lookup"><span data-stu-id="aaf97-109">To remove this requirement, set the **pwdLastSet** attribute to -1.</span></span> <span data-ttu-id="aaf97-110">El atributo **pwdLastSet** no se puede establecer en ningún otro valor excepto en el sistema.</span><span class="sxs-lookup"><span data-stu-id="aaf97-110">The **pwdLastSet** attribute cannot be set to any other value except by the system.</span></span>

<span data-ttu-id="aaf97-111">En el ejemplo de código siguiente se muestra cómo establecer la opción "el usuario debe cambiar la contraseña en el siguiente inicio de sesión".</span><span class="sxs-lookup"><span data-stu-id="aaf97-111">The following code example shows how to set the "User must change password at next logon" option.</span></span>


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



<span data-ttu-id="aaf97-112">En el ejemplo de código siguiente se muestra cómo establecer la opción "el usuario debe cambiar la contraseña en el siguiente inicio de sesión".</span><span class="sxs-lookup"><span data-stu-id="aaf97-112">The following code example shows how to set the "User must change password at next logon" option.</span></span>


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




