---
description: 'Más información sobre: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)'
title: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Single)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100877
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
ms.openlocfilehash: e57a42a46b9247133c1427f3ae270645f6133523
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072620"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-single"></a>Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)

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
    data As Single _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As SingleApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    float data
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
    Tipo: [System.Single](/dotnet/api/system.single)  
    
    Datos que se van a establecer.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de SetColumn](./api.setcolumn-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
