---
description: 'Más información sobre: Método Api.JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)'
title: Método Api.JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b7ea09ae36160fc83fbee4dc3b7f94222f55125b992039aa15035c1d958c696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117718723"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a>Método Api.JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)

Navegue por un índice. El cursor se puede colocar al principio o al final del índice y moverse hacia atrás y hacia delante mediante un número especificado de entradas de índice. Vea también [TryMoveFirst(JET_SESID, JET_TABLEID),](./api.trymovefirst-method.md) [TryMoveLast(JET_SESID, JET_TABLEID),](./api.trymovelast-method.md) [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID).](./api.trymoveprevious-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará para la llamada.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se colocará.

<!-- end list -->

  - numRows  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)  
    
    Desplazamiento que indica hasta dónde mover el cursor.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)  
    
    Opciones de movimiento.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetMove](./api.jetmove-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
