---
title: Cuenta deshabilitada (proveedor de WinNT)
description: Cuando se usa el proveedor de WinNT, se puede habilitar o deshabilitar una cuenta mediante la propiedad IADsUser. AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Cuenta deshabilitada (proveedor de WinNT)
- Cuenta ADSI deshabilitada, proveedor de Winnt
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, cuenta deshabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424303"
---
# <a name="account-disabled-winnt-provider"></a><span data-ttu-id="345a9-106">Cuenta deshabilitada (proveedor de WinNT)</span><span class="sxs-lookup"><span data-stu-id="345a9-106">Account Disabled (WinNT Provider)</span></span>

<span data-ttu-id="345a9-107">Cuando se usa el proveedor de WinNT, se puede habilitar o deshabilitar una cuenta mediante la propiedad [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="345a9-107">When using the WinNT provider, an account can be enabled or disabled using the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property.</span></span>

## <a name="example-1"></a><span data-ttu-id="345a9-108">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="345a9-108">Example 1</span></span>

<span data-ttu-id="345a9-109">En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta mediante Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="345a9-109">The following code example shows how to disable an account using Visual Basic with ADSI.</span></span>


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="345a9-110">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="345a9-110">Example 2</span></span>

<span data-ttu-id="345a9-111">En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta mediante C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="345a9-111">The following code example shows how to disable an account using C++ with ADSI.</span></span>


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




