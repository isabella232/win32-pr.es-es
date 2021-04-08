---
description: 'Más información sobre: método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100838
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3bc5db8aa14f3cabf05f15f8e1ecb41256496b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003001"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid"></a>Método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)

Recupera un valor de columna de bytes del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
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

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\>  
Los datos recuperados de la columna como un byte. Es NULL si la columna es NULL.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga RetrieveColumnAsByte](./api.retrievecolumnasbyte-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
