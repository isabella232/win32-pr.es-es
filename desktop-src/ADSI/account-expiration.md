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
# <a name="account-expiration-ldap-provider"></a><span data-ttu-id="a1e1e-105">Expiración de la cuenta (proveedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="a1e1e-105">Account Expiration (LDAP Provider)</span></span>

<span data-ttu-id="a1e1e-106">Para establecer la fecha de expiración de la cuenta, establezca la propiedad [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) en el valor de fecha deseado.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-106">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="a1e1e-107">Para deshabilitar la fecha de expiración de la cuenta, establezca el atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) en cero.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-107">To disable the account expiration date, set the [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute to zero.</span></span> <span data-ttu-id="a1e1e-108">En los siguientes ejemplos de código se muestra cómo establecer la fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-108">The following code examples show how to set the expiration date.</span></span>


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
> <span data-ttu-id="a1e1e-109">El atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contiene la fecha de expiración de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-109">The [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute contains the account expire date.</span></span> <span data-ttu-id="a1e1e-110">El complemento MMC Active Directory usuarios y equipos muestra la fecha en la que expirará la cuenta al final de.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-110">The Active Directory Users and Computers MMC snap-in displays the date that the account will expire at the end of.</span></span> <span data-ttu-id="a1e1e-111">Es decir, el complemento MMC usuarios y equipos de Active Directory mostrará la fecha de expiración de la cuenta como un día anterior a la fecha incluida en el atributo **accountExpires** .</span><span class="sxs-lookup"><span data-stu-id="a1e1e-111">That is, the Active Directory Users and Computers MMC snap-in will display the account expiration date as one day earlier than the date contained in the **accountExpires** attribute.</span></span>

 

 

 