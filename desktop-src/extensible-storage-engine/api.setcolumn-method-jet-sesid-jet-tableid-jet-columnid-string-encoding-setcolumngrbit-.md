---
description: 'Más información sobre: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)'
title: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100886
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a6588d85b546432612ba6b2c5e7230d8022de5b42aa643f68f447c14210d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717471"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding-setcolumngrbit"></a>Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)

Modifica un valor de columna única en un registro modificado que se va a insertar o para actualizar el registro actual.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding, _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As Encoding
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, encoding, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding,
    SetColumnGrbit grbit
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

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se establecerá.

<!-- end list -->

  - datos  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Datos que se van a establecer.

<!-- end list -->

  - encoding  
    Tipo: [System.Text.Encoding](/dotnet/api/system.text.encoding)  
    
    Codificación utilizada para convertir la cadena.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)  
    
    Opciones de SetColumn.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de SetColumn](./api.setcolumn-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
