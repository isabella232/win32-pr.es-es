---
description: 'Más información sobre: Campo Server2003Grbits.WaitAllLevel0Commit'
title: Campo Server2003Grbits.WaitAllLevel0Commit (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c6f3946d12b7614818545abc785d521e46b9c05ddedcffab09750846861782e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093175"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Campo Server2003Grbits.WaitAllLevel0Commit

Todas las transacciones confirmadas previamente por cualquier sesión que aún no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esta opción se puede usar incluso si la sesión no está actualmente en una transacción. Esta opción no se puede usar en combinación con ninguna otra opción.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Server2003Grbits (clase)](./server2003grbits-class.md)

[Miembros server2003Grbits](./server2003grbits-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
