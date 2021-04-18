---
description: 'Más información acerca de: JetDeleteTable (función)'
title: JetDeleteTable función)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717235"
---
# <a name="jetdeletetable-function"></a>JetDeleteTable función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>JetDeleteTable función)

La función **JetDeleteTable** elimina una tabla en una base de datos ese.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*DBID*

Identificador de base de datos que se va a usar para la llamada API.

*szTableName*

Nombre de la tabla que se va a eliminar.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Se intentó eliminar una tabla mientras otra tiene un ID. de tabla abierta (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) con <a href="gg294118(v=exchg.10).md">JetOpenTable</a> o <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeletetemporary tabla</p></td>
<td><p>Se intentó eliminar una tabla temporal. Una tabla temporal se elimina automáticamente cuando se cierra con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable</p></td>
<td><p>Se intentó eliminar una tabla de plantilla, es decir, una tabla de la que se puede heredar DDL.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetDeleteTableW</strong> (Unicode) y <strong>JetDeleteTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
