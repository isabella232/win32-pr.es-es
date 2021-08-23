---
description: Más información sobre el método Server2003Api.JetUpdate2
title: Método Server2003Api.JetUpdate2 (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f19d0bb4ab599e2f7a11ac66202c805066c1744b80ed72223d20be423340d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978575"
---
# <a name="server2003apijetupdate2-method"></a>Método Server2003Api.JetUpdate2

La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. La eliminación de una fila de tabla se realiza mediante una llamada [a JetDelete(JET_SESID, JET_TABLEID).](./api.jetdelete-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que inició la actualización.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se actualizará. Se debe preparar una actualización.

<!-- end list -->

  - marcador  
    Tipo: \[\]  
    
    Devuelve el marcador del registro actualizado. Puede ser NULL.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer de marcador.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el tamaño real del marcador.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)  
    
    Opciones de actualización.

## <a name="remarks"></a>Comentarios

JetUpdate es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y, a continuación, llamando a [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o más veces para establecer el estado del registro. Por último, se llama a JetUpdate2(JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) para completar la operación de actualización. Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Server2003Api](./server2003api-class.md)

[Miembros Server2003Api](./server2003api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
