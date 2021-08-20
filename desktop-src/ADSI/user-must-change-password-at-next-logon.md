---
title: El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor LDAP)
description: Para forzar a un usuario a cambiar su contraseña en el siguiente inicio de sesión, establezca el atributo pwdLastSet en cero (0). Para quitar este requisito, establezca el atributo pwdLastSet en -1. El atributo pwdLastSet no se puede establecer en ningún otro valor excepto por el sistema.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- El usuario debe cambiar la contraseña en el siguiente inicio de sesión ADSI, proveedor LDAP
- ADSI del proveedor LDAP, ejemplos de administración de usuarios, Usuario debe cambiar la contraseña en el siguiente inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103703381512e82eee608d452b921429c87ef3ce6b7d59017fd07bc081e75ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648845"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor LDAP)

Para forzar a un usuario a cambiar su contraseña en el siguiente inicio de sesión, establezca el atributo **pwdLastSet** en cero (0). Para quitar este requisito, establezca el **atributo pwdLastSet** en -1. El **atributo pwdLastSet** no se puede establecer en ningún otro valor excepto por el sistema.

En el ejemplo de código siguiente se muestra cómo establecer la opción "El usuario debe cambiar la contraseña en el siguiente inicio de sesión".


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



En el ejemplo de código siguiente se muestra cómo establecer la opción "El usuario debe cambiar la contraseña en el siguiente inicio de sesión".


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



 

 




