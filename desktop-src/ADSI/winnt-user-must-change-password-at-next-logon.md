---
title: El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor de WinNT)
description: Para habilitar esta opción, establezca el atributo PasswordExpired del usuario en uno (1). Establecer este atributo en cero (0) permite que el usuario inicie sesión sin cambiar la contraseña.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor WinNT) ADSI
- El usuario debe cambiar la contraseña en el siguiente inicio de sesión ADSI, proveedor de Winnt
- ADSI Provider ADSI, ejemplos de administración de usuarios, el usuario debe cambiar la contraseña en el siguiente inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660093"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="2161f-107">El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor de WinNT)</span><span class="sxs-lookup"><span data-stu-id="2161f-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="2161f-108">Para habilitar esta opción, establezca el atributo **PasswordExpired** del usuario en uno (1).</span><span class="sxs-lookup"><span data-stu-id="2161f-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="2161f-109">Establecer este atributo en cero (0) permite que el usuario inicie sesión sin cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2161f-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="2161f-110">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2161f-110">Example 1</span></span>

<span data-ttu-id="2161f-111">En el ejemplo de código siguiente se muestra cómo establecer la opción cambiar contraseña en el siguiente inicio de sesión mediante Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="2161f-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="2161f-112">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2161f-112">Example 2</span></span>

<span data-ttu-id="2161f-113">En el ejemplo de código siguiente se muestra cómo establecer la opción cambiar contraseña en el siguiente inicio de sesión con C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="2161f-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




