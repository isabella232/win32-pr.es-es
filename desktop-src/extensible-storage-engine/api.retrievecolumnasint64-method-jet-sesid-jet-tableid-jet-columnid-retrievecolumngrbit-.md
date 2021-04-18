---
description: 'Más información sobre: método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100891
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 158e350dc3d85b99b4651c448c8b1b7d51a1ce14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697636"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor del que se va a recuperar la columna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se va a recuperar.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Opciones de recuperación.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\>  
Los datos recuperados de la columna como un valor Long. Es NULL si la columna es NULL.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga RetrieveColumnAsInt64](./api.retrievecolumnasint64-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
