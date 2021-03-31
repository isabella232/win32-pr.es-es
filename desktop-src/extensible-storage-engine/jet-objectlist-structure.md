---
description: 'Más información acerca de: estructura de JET_OBJECTLIST'
title: Estructura de JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361102"
---
# <a name="jet_objectlist-structure"></a>Estructura de JET_OBJECTLIST


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_objectlist-structure"></a>Estructura de JET_OBJECTLIST

La estructura **JET_OBJECTLIST** atraviesa una tabla temporal que se creó con [JetGetObjectInfo](./jetgetobjectinfo-function.md). Cada fila de la tabla temporal describe un objeto de la base de datos.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura, en bytes. La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_INDEXLIST).

**TABLEID**

Identificador de tabla de la tabla temporal que se creó. El autor de la llamada debe contener código que cierre la tabla.

**cRecord**

El número de registros de la tabla temporal que se creó.

**columnidcontainername**

Identificador de columna del nombre del tipo de contenedor.

Los únicos contenedores que se admiten actualmente son tablas. Esta columna es un [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Identificador de columna del nombre del objeto.

Esta columna es un [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

Identificador de columna del tipo del objeto. Los únicos contenedores que se admiten actualmente son tablas, por lo que este campo se JET_objtypTable.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsoleto. No debe usarse.

**columniddtUpdate**

Obsoleto. No debe usarse.

**columnidgrbit**

Identificador de columna del **grbits** que se aplica al objeto. Para obtener una lista de los **grbits** aplicables, consulte [JET_TABLECREATE](./jet-tablecreate-structure.md).

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

El identificador de columna de las marcas que se aplican al objeto. Para obtener una lista de las marcas aplicables, vea [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

El identificador de columna del número de registros que se encuentran en la tabla con el nombre en **columnidobjectname**.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificador de columna del número de páginas que utiliza el objeto.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Observaciones

Cada fila de la tabla temporal corresponde a un objeto de la base de datos.

Cuando se crea la tabla temporal con el parámetro *InfoLevel* en la función [JetGetObjectInfo](./jetgetobjectinfo-function.md) establecida en JET_ObjInfoListNoStats, las columnas identificadas por **columnidcRecord** y **columnidcPage** no contendrán información significativa.

Actualmente, solo la información sobre las tablas estará en la tabla temporal.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
