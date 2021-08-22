---
title: El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor winNT)
description: Para habilitar esta opción, establezca el atributo PasswordExpired del usuario en uno (1). Establecer este atributo en cero (0) permite al usuario iniciar sesión sin cambiar la contraseña.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor winNT) ADSI
- El usuario debe cambiar la contraseña en el siguiente adsi de inicio de sesión, proveedor de WinNT
- ADSI del proveedor winNT, ejemplos de administración de usuarios, usuario debe cambiar la contraseña en el siguiente inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023043"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>El usuario debe cambiar la contraseña en el siguiente inicio de sesión (proveedor winNT)

Para habilitar esta opción, establezca el **atributo PasswordExpired** del usuario en uno (1). Establecer este atributo en cero (0) permite al usuario iniciar sesión sin cambiar la contraseña.

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo establecer la opción cambiar contraseña en el siguiente inicio de sesión mediante Visual Basic con ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se muestra cómo establecer la opción cambiar contraseña en el siguiente inicio de sesión mediante C++ con ADSI.


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



 

 




