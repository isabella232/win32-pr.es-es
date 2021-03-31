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
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="df1fc-105">SID de objeto (proveedor WinNT)</span><span class="sxs-lookup"><span data-stu-id="df1fc-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="df1fc-106">El identificador de seguridad (SID) del usuario se puede recuperar mediante el atributo **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="df1fc-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="df1fc-107">El **objectSid** se devuelve como una matriz **variante** de caracteres que forman la cadena SID.</span><span class="sxs-lookup"><span data-stu-id="df1fc-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="df1fc-108">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="df1fc-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




