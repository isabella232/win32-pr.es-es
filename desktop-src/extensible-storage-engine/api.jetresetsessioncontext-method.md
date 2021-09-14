---
description: Más información sobre el método Api.JetResetSessionContext
title: Método Api.JetResetSessionContext
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240753"
---
# <a name="apijetresetsessioncontext-method"></a>Método Api.JetResetSessionContext

Desasocia una sesión del subproceso actual. Debe usarse junto con [JetSetSessionContext(JET_SESID, IntPtr).](./api.jetsetsessioncontext-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
