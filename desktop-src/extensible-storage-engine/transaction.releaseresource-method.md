---
description: Más información sobre el método Transaction.ReleaseResource
title: Método Transaction.ReleaseResource
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78d3dc358b6c7c5dfe297132fd83f08c64693c85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473147"
---
# <a name="transactionreleaseresource-method"></a>Método Transaction.ReleaseResource

Se llama cuando la transacción se elimina mientras está activa. Esto debería revertir la transacción.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Transaction, clase](./transaction-class.md)

[Miembros de transacción](./transaction-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
