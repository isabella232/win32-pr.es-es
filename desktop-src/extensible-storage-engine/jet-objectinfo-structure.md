---
description: 'Más información acerca de: estructura de JET_OBJECTINFO'
title: Estructura de JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083049"
---
# <a name="jet_objectinfo-structure"></a>Estructura de JET_OBJECTINFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>Estructura de JET_OBJECTINFO

La estructura de **JET_OBJECTINFO** contiene información sobre un objeto. Las tablas son los únicos tipos de objeto que se admiten actualmente.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, de la estructura de **JET_OBJECTINFO** .

**objtyp**

Contiene el [JET_OBJTYP](./jet-objtyp.md) de la estructura. Actualmente solo se devolverán las tablas (es decir, JET_objtypTable).

**dtCreate**

Obsoleto. No debe usarse.

**dtUpdate**

Obsoleto. No debe usarse.

**grbit**

Grupo de bits que contiene las opciones disponibles para esta llamada, que incluyen cero o más de los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>La tabla puede tener marcadores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>La tabla se puede revertir.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>Se puede actualizar la tabla.</p></td>
</tr>
</tbody>
</table>


**flags**

Campo de bits que contiene cero o más de los siguientes marcadores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitObjectSystem</p></td>
<td><p>La tabla es una tabla del sistema y solo es para uso interno.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>La tabla DDL heredado de una tabla de plantilla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>No se puede modificar el DDL de la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Se usa junto con JET_bitObjectTableTemplate para no permitir columnas fijas o variables en las tablas derivadas (de modo que se puedan agregar columnas fijas o de variables a la plantilla en el futuro).</p>
<p><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>La tabla es una tabla de plantillas.</p></td>
</tr>
</tbody>
</table>


**cRecord**

Número de registros de la tabla.

Este valor se recupera solo si **JET_OBJECTINFO** se pasó a [JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

Número de páginas que utiliza la tabla.

Este valor se recupera solo si **JET_OBJECTINFO** se pasó a [JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Observaciones

Una estructura de **JET_OBJECTINFO** se rellena mediante una llamada a [JetGetObjectInfo](./jetgetobjectinfo-function.md) o [JetGetTableInfo](./jetgettableinfo-function.md). Si la llamada a la API no se realiza correctamente, el contenido de la estructura es indefinido.

Si procede, las estadísticas de la tabla incluyen el número de registros y el número de páginas que se encuentran en el índice clúster (es decir, el índice que contiene los datos del registro). Se tiene acceso a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

### <a name="requirements"></a>Requisitos

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
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
