---
description: 'Más información sobre: Método Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)'
title: Método Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90fd53fd7097db98ab84148b3f32710c369c948ed64c3606d0018cc8e79c877a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890518"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Método Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)

Confirmar una transacción. Este objeto debe estar en una transacción.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parámetros

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Opciones de JetCommitTransaction.

<!-- end list -->

  - durableCommit  
    Tipo: [System.TimeSpan](/dotnet/api/system.timespan)  
    
    Duración de la confirmación de transacciones diferida.

<!-- end list -->

  - commitId  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Commit-id para este registro de confirmación.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Transaction, clase](./transaction-class.md)

[Miembros de transacción](./transaction-members.md)

[Sobrecarga de confirmación](./transaction.commit-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
