---
title: SID de objeto (proveedor WinNT)
description: El identificador de seguridad (SID) del usuario se puede recuperar mediante el atributo objectSID. El objectSID se devuelve como una matriz variante de caracteres que forman la cadena SID.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, SID de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075070"
---
# <a name="object-sid-winnt-provider"></a>SID de objeto (proveedor WinNT)

El identificador de seguridad (SID) del usuario se puede recuperar mediante el atributo **objectSid** . El **objectSid** se devuelve como una matriz **variante** de caracteres que forman la cadena SID.

## <a name="example-code"></a>Código de ejemplo


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




