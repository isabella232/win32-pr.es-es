---
description: 'Más información sobre: Método Api.RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método Api.RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be97e5e683c14a3b2f6adca300e9a78e0afaac10129f071114c62097a45bf7bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084630"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Método Api.RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Recupera un valor de columna datetime del registro actual. El registro es ese registro asociado a la entrada de índice en la posición actual del cursor.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor del que se recuperará la columna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se recuperará.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Opciones de recuperación.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Los datos recuperados de la columna como datetime. Null si la columna es NULL.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga RetrieveColumnAsDateTime](./api.retrievecolumnasdatetime-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
