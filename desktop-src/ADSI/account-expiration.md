---
title: Expiración de la cuenta (proveedor LDAP)
description: Para establecer la fecha de expiración de la cuenta, establezca la propiedad IADsUser.AccountExpirationDate en el valor de fecha deseado.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Proveedor ADSI,LDAP de expiración de la cuenta
- ADSI del proveedor LDAP, ejemplos de administración de usuarios, expiración de la cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645ce5e2e1ae72ace0a8a642642eb5c15e7eabd63d51dba3f03596869bfb9efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024073"
---
# <a name="account-expiration-ldap-provider"></a>Expiración de la cuenta (proveedor LDAP)

Para establecer la fecha de expiración de la cuenta, establezca la propiedad [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) en el valor de fecha deseado. Para deshabilitar la fecha de expiración de la cuenta, establezca el [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) en cero. En los ejemplos de código siguientes se muestra cómo establecer la fecha de expiración.


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> El [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contiene la fecha de expiración de la cuenta. El Usuarios y equipos de Active Directory complemento MMC muestra la fecha de expiración de la cuenta al final. Es decir, Usuarios y equipos de Active Directory complemento MMC mostrará la fecha de expiración de la cuenta como un día anterior a la fecha contenida en el atributo **accountExpires.**

 

 

 