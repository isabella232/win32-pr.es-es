---
description: 'Más información sobre: método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100870
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7176fa1c78b9910b68d0b3c9e7ce4f7e46519020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720300"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid"></a>Método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)

Recupera un valor de columna DateTime del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
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

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Los datos recuperados de la columna como un valor de fecha y hora. Es NULL si la columna es NULL.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga RetrieveColumnAsDateTime](./api.retrievecolumnasdatetime-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
