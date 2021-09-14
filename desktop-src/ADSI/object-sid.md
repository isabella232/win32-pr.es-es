---
title: SID de objeto (proveedor winNT)
description: El identificador de seguridad de usuario (SID) se puede recuperar mediante el atributo objectSID. ObjectSID se devuelve como una matriz VARIANT de caracteres que forman la cadena SID.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- ADSI del proveedor WinNT, ejemplos de administración de usuarios, SID de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887100"
---
# <a name="object-sid-winnt-provider"></a>SID de objeto (proveedor winNT)

El identificador de seguridad de usuario (SID) se puede recuperar mediante el **atributo objectSID.** **ObjectSID se** devuelve como una **matriz VARIANT** de caracteres que forman la cadena SID.

## <a name="example-code"></a>Código de ejemplo


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




