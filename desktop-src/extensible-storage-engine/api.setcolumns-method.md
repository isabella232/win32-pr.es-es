---
description: 'Más información sobre: Método Api.SetColumns'
title: Método Api.SetColumns
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d1fa66826fc32c02d8a33fb42d86e1ad0ca62941c52c8cc432fadb10a99466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738635"
---
# <a name="apisetcolumns-method"></a>Método Api.SetColumns

Establece columnas a partir de objetos ColumnValue.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se actualizará. Se debe preparar una actualización.

<!-- end list -->

  - valores  
    Tipo: \[\]  
    
    Valores que se establecerán.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
