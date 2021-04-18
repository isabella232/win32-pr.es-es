---
description: 'Más información sobre: método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100669
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe2bb9757216dc4b0a671ae9d5da6cdf4bd5eb7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714952"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Método API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Deserializa un objeto de una columna.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Object DeserializeObjectFromColumn(
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
    
    Tabla de la que se va a leer.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columna desde la que se va a leer.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Opciones de recuperación que se van a utilizar.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Object](/dotnet/api/system.object)  
Objeto deserializado. Es NULL si la columna era null.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga DeserializeObjectFromColumn](./api.deserializeobjectfromcolumn-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
