---
description: 'Más información sobre: enumeración JET_TblInfo datos'
title: JET_TblInfo enumeración
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b2af9bfd69f81b518eba42f435a457c9baaa0d0ce8ddbac1424b997329a3ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832685"
---
# <a name="jet_tblinfo-enumeration"></a>JET_TblInfo enumeración

Niveles de información para recuperar información de tabla con JetGetTableInfo.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a>Miembros

<table>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Valor predeterminado</td>
<td>Opciones predeterminadas Recupera un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> que contiene información sobre la tabla. Use esta opción con <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>Nombre</td>
<td>Recupera el nombre de la tabla. Use esta opción con <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Recupera el <a href="hh596176(v=exchg.10).md">JET_DBID</a> de la base de datos que contiene la tabla. Use esta opción con <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>El comportamiento del método depende del tamaño de la matriz que se pasa al método. La matriz debe tener al menos dos entradas. La primera entrada contendrá el número de extensiones de propiedad de la tabla. La segunda entrada contendrá el número de extensiones disponibles en la tabla. Si la matriz tiene más de dos entradas, los bytes restantes del búfer contendrán una matriz de estructuras que representan una lista de extensiones. Esta estructura contiene dos miembros: el último número de página de la extensión y el número de páginas de la extensión. Use esta opción con <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>La matriz que se pasa a JetGetTableInfo debe tener dos entradas. La primera entrada se establecerá en el número de páginas de la tabla. La segunda entrada se establecerá en la densidad de destino de las páginas de la tabla. Use esta opción con <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>Obtiene el número de páginas de propiedad de la tabla. Use esta opción con <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>Espacio disponible</td>
<td>Obtiene el número de páginas disponibles en la tabla. Use esta opción con <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>Si la tabla es una tabla derivada, el resultado se rellenará con el nombre de la tabla de la que la tabla derivada heredó su DDL. Si la tabla no es una tabla derivada, el búfer será una cadena vacía. Use esta opción con <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo).</a></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
