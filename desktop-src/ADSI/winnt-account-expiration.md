---
title: Expiración de la cuenta (proveedor WinNT)
description: Cuando se usa el proveedor de WinNT, la fecha de expiración de la cuenta se puede establecer mediante la propiedad IADsUser. AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Caducidad de cuenta ADSI, proveedor de Winnt
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, expiración de cuentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660095"
---
# <a name="account-expiration-winnt-provider"></a>Expiración de la cuenta (proveedor WinNT)

Cuando se usa el proveedor de WinNT, la fecha de expiración de la cuenta se puede establecer mediante la propiedad [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) .

Para establecer la fecha de expiración de la cuenta, establezca la propiedad [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) en el valor de fecha deseado. Para establecer que la fecha de expiración de la cuenta no expire nunca, establezca esta propiedad en "1 de enero de 1970".

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo establecer la fecha de expiración de la cuenta mediante Visual Basic con ADSI.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se muestra cómo establecer la fecha de expiración de la cuenta mediante C++ con ADSI.


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




