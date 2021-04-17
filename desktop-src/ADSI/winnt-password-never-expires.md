---
title: La contraseña nunca expira (proveedor de WinNT)
description: Para habilitar esta opción mediante el proveedor ADSI de WinNT, establezca la \_ marca ADS up no \_ \_ expire \_ (0x10000) en el atributo UserFlags. Nota para Windows 2000 y versiones posteriores, use el proveedor ADSI LDAP para las operaciones de administración de usuarios, como se muestra.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- La contraseña nunca expira (proveedor de WinNT)
- La contraseña nunca expira ADSI, el proveedor de Winnt
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, la contraseña nunca expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660094"
---
# <a name="password-never-expires-winnt-provider"></a>La contraseña nunca expira (proveedor de WinNT)

Para habilitar esta opción mediante el proveedor ADSI de WinNT, establezca la marca **ADS \_ up no \_ \_ expire \_** (0x10000) en el atributo **UserFlags** .

> [!Note]  
> En Windows 2000 y versiones posteriores, use el proveedor ADSI LDAP para las operaciones de administración de usuarios, como se muestra. Para obtener más información, consulte la [contraseña nunca expira (proveedor LDAP)](password-never-expires.md).

 

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo establecer la opción la contraseña nunca expira mediante Visual Basic con ADSI.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se muestra cómo establecer la opción la contraseña nunca expira con C++ con ADSI.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




