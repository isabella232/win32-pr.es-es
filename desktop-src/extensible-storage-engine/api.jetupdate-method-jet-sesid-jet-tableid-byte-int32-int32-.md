---
description: 'Más información sobre: Método Api.JetUpdate (JET_SESID, JET_TABLEID, Byte , Int32, Int32)'
title: Método Api.JetUpdate (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072632"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>Método Api.JetUpdate (JET_SESID, JET_TABLEID, Byte , Int32, Int32)

La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. La eliminación de una fila de tabla se realiza mediante una llamada [a JetDelete(JET_SESID, JET_TABLEID).](./api.jetdelete-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
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

## <a name="remarks"></a>Observaciones

JetUpdate es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y, a continuación, llamando a [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o más veces para establecer el estado del registro. Por último, se llama a JetUpdate(JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) para completar la operación de actualización. Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetUpdate](./api.jetupdate-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
