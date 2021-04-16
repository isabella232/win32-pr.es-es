---
title: Bloqueo de cuenta (proveedor de WinNT)
description: Cuando se supera el número de intentos de inicio de sesión erróneos, la cuenta de usuario se bloquea durante el número de minutos especificado por el atributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Bloqueo de cuenta ADSI, proveedor de Winnt
- ADSI del proveedor de WinNT, ejemplos de administración de usuarios, bloqueo de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656411"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="e2aba-105">Bloqueo de cuenta (proveedor de WinNT)</span><span class="sxs-lookup"><span data-stu-id="e2aba-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="e2aba-106">Cuando se supera el número de intentos de inicio de sesión erróneos, la cuenta de usuario se bloquea durante el número de minutos especificado por el atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="e2aba-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="e2aba-107">La propiedad [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser la propiedad que se va a usar para leer y modificar el estado de bloqueo de una cuenta de usuario, pero el proveedor ADSI de WinNT tiene restricciones que limitan el uso de la propiedad **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="e2aba-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="e2aba-108">Restableciendo el estado de bloqueo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e2aba-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="e2aba-109">Cuando se usa el proveedor de WinNT, la propiedad [**IsAccountLocked**](iadsuser-property-methods.md) solo se puede establecer en **false**, lo que desbloquea la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e2aba-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="e2aba-110">Se producirá un error al intentar establecer la propiedad **IsAccountLocked** en **true** .</span><span class="sxs-lookup"><span data-stu-id="e2aba-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="e2aba-111">Solo el sistema puede bloquear una cuenta.</span><span class="sxs-lookup"><span data-stu-id="e2aba-111">Only the system can lock an account.</span></span>

<span data-ttu-id="e2aba-112">En el ejemplo de código siguiente se muestra cómo usar Visual Basic con ADSI para desbloquear una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e2aba-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



<span data-ttu-id="e2aba-113">En el ejemplo de código siguiente se muestra cómo utilizar C++ con ADSI para desbloquear una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e2aba-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="e2aba-114">Leer el estado de bloqueo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e2aba-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="e2aba-115">Con el proveedor de WinNT, la propiedad [**IsAccountLocked**](iadsuser-property-methods.md) se puede usar para determinar si una cuenta está bloqueada. Si una cuenta está bloqueada, la propiedad **IsAccountLocked** contendrá **true**.</span><span class="sxs-lookup"><span data-stu-id="e2aba-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="e2aba-116">Si una cuenta no está bloqueada, la propiedad **IsAccountLocked** contendrá **false**.</span><span class="sxs-lookup"><span data-stu-id="e2aba-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="e2aba-117">En el ejemplo de código siguiente se muestra cómo usar Visual Basic con ADSI para determinar si una cuenta está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e2aba-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="e2aba-118">En el ejemplo de código siguiente se muestra cómo utilizar C++ con ADSI para determinar si una cuenta está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e2aba-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 