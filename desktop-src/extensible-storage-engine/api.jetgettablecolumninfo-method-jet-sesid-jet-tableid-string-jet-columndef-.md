---
description: 'Más información sobre: método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, cadena, JET_COLUMNDEF)'
title: Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, cadena, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100724
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60e984fdb1577dc69a352c327c1af605e0d441d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360449"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columndef"></a>Método API. JetGetTableColumnInfo (JET_SESID, JET_TABLEID, cadena, JET_COLUMNDEF)

Recupera información sobre una columna de la tabla.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla que contiene la columna.

<!-- end list -->

  - columnName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    El nombre de la columna.

<!-- end list -->

  - columndef  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    Se rellena con información sobre la columna.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetGetTableColumnInfo](./api.jetgettablecolumninfo-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
