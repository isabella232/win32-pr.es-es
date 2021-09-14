---
description: 'Más información sobre: Método Api.JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)'
title: Método Api.JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100723
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
ms.openlocfilehash: 516dad3bbc93a12ec216c5c3caa35617ea989bbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969460"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columnlist"></a>Método Api.JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)

Recupera información sobre todas las columnas de la tabla.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columnlist)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla que contiene la columna.

<!-- end list -->

  - columnName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Se omite el parámetro.

<!-- end list -->

  - columnlist  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)  
    
    Rellenado con información sobre las columnas de la tabla.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetGetTableColumnInfo](./api.jetgettablecolumninfo-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
