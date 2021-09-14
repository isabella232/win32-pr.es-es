---
description: Más información sobre el método Api.JetSetSessionContext
title: Método Api.JetSetSessionContext
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063667"
---
# <a name="apijetsetsessioncontext-method"></a>Método Api.JetSetSessionContext

Asocia una sesión al subproceso actual mediante el identificador de contexto especificado. Esta asociación invalida el requisito predeterminado del motor de que una transacción para una sesión determinada debe producirse completamente en el mismo subproceso. Use [JetResetSessionContext(JET_SESID) para](./api.jetresetsessioncontext-method.md) quitar la asociación.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión en la que se establece el contexto.

<!-- end list -->

  - context  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contexto que se establecerá.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
