---
description: 'Más información sobre: Windows8Api. JetCommitTransaction2 (método)'
title: Método Windows8Api. JetCommitTransaction2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705866"
---
# <a name="windows8apijetcommittransaction2-method"></a>Windows8Api. JetCommitTransaction2, método

Confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior. Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión para la que se va a confirmar la transacción.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Opciones de confirmación.

<!-- end list -->

  - durableCommit  
    Tipo: [System. TimeSpan](/dotnet/api/system.timespan)  
    
    Duración de la confirmación de transacción diferida.

<!-- end list -->

  - commitId  
    Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    ID. de confirmación asociado a este registro de confirmación.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Windows8Api](./windows8api-class.md)

[Miembros de Windows8Api](./windows8api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
