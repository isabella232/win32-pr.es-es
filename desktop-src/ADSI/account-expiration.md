---
title: Expiración de la cuenta (proveedor LDAP)
description: Para establecer la fecha de expiración de la cuenta, establezca la propiedad IADsUser. AccountExpirationDate en el valor de fecha deseado.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Caducidad de cuenta ADSI, proveedor LDAP
- ADSI Provider LDAP, ejemplos de administración de usuarios, expiración de cuentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656399"
---
# <a name="account-expiration-ldap-provider"></a>Expiración de la cuenta (proveedor LDAP)

Para establecer la fecha de expiración de la cuenta, establezca la propiedad [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) en el valor de fecha deseado. Para deshabilitar la fecha de expiración de la cuenta, establezca el atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) en cero. En los siguientes ejemplos de código se muestra cómo establecer la fecha de expiración.


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
> El atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contiene la fecha de expiración de la cuenta. El complemento MMC Active Directory usuarios y equipos muestra la fecha en la que expirará la cuenta al final de. Es decir, el complemento MMC usuarios y equipos de Active Directory mostrará la fecha de expiración de la cuenta como un día anterior a la fecha incluida en el atributo **accountExpires** .

 

 

 