---
title: La contraseña nunca expira (proveedor winNT)
description: Para habilitar esta opción mediante el proveedor ADSI de WinNT, establezca la marca ADS \_ UF \_ DONT EXPIRE PASSWD (0x10000) en el \_ atributo \_ UserFlags. Nota Para Windows 2000 y versiones posteriores, use el proveedor ADSI LDAP para las operaciones de administración de usuarios como se muestra.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- La contraseña nunca expira (proveedor winNT)
- Password Never Expires ADSI , WinNT provider
- ADSI del proveedor WinNT, ejemplos de administración de usuarios, Contraseña nunca expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47cdd7dc181c2875e8de06b66233d727c5b132963921b163b02fc09cbdc051d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082169"
---
# <a name="password-never-expires-winnt-provider"></a>La contraseña nunca expira (proveedor winNT)

Para habilitar esta opción mediante el proveedor ADSI de WinNT, establezca la marca **ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD** (0x10000) en el **atributo UserFlags.**

> [!Note]  
> Para Windows 2000 y versiones posteriores, use el proveedor ADSI LDAP para las operaciones de administración de usuarios como se muestra. Para obtener más información, vea [Password Never Expires (LDAP Provider) (La contraseña nunca expira [proveedor LDAP]).](password-never-expires.md)

 

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo establecer la opción password never expires mediante Visual Basic con ADSI.


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

En el ejemplo de código siguiente se muestra cómo establecer la opción password never expires mediante C++ con ADSI.


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



 

 




