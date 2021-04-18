---
title: Cuenta deshabilitada (proveedor LDAP)
description: Para deshabilitar una cuenta de usuario, establezca la propiedad AccountDisabled en TRUE en la interfaz IADsUser. Esto es similar al proveedor de Winnt. En los siguientes ejemplos de código se muestra cómo deshabilitar una cuenta de usuario.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Cuenta ADSI deshabilitada, proveedor LDAP
- ADSI Provider LDAP, ejemplos de administración de usuarios, cuenta deshabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660097"
---
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="ce422-107">Cuenta deshabilitada (proveedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="ce422-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="ce422-108">Para deshabilitar una cuenta de usuario, establezca la propiedad AccountDisabled en **true** en la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="ce422-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="ce422-109">Esto es similar al proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="ce422-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="ce422-110">En los siguientes ejemplos de código se muestra cómo deshabilitar una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce422-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="ce422-111">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce422-111">Example 1</span></span>


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="ce422-112">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce422-112">Example 2</span></span>


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




