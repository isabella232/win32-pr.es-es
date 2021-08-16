---
title: La contraseña nunca expira (proveedor LDAP)
description: Para habilitar la opción password never expires mediante el proveedor LDAP, establezca la marca ADS UF DONT EXPIRE PASSWD en el \_ \_ atributo \_ \_ userAccountControl del usuario.
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- La contraseña nunca expira en el proveedor ADSI y LDAP
- ADSI del proveedor LDAP, ejemplos de administración de usuarios,Contraseña nunca expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa48145fa2b78c7685cdf52ab58b1e681df48c7d10a80f0ac7462fa7d4cb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838935"
---
# <a name="password-never-expires-ldap-provider"></a>La contraseña nunca expira (proveedor LDAP)

Para habilitar la opción password never expires mediante el proveedor LDAP, establezca la marca [**ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) en el [**atributo userAccountControl del**](/windows/desktop/ADSchema/a-useraccountcontrol) usuario.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 