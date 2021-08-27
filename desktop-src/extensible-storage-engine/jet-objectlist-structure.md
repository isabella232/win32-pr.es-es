---
description: 'Más información sobre: JET_OBJECTLIST estructura'
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
ms.openlocfilehash: 21a3ea030421406a5bc571bb5cc1887f77b4710d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983128"
---
# <a name="jet_objectlist-structure"></a>Estructura de JET_OBJECTLIST


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_objectlist-structure"></a>Estructura de JET_OBJECTLIST

La **JET_OBJECTLIST** recorre una tabla temporal que se creó [con JetGetObjectInfo](./jetgetobjectinfo-function.md). Cada fila de la tabla temporal describe un objeto de la base de datos.

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

Tamaño de la estructura, en bytes. La llamada API actualizará este campo, por lo que el autor de la llamada debe asegurarse de que este valor coincide con sizeof( JET_INDEXLIST ).

**tableid**

Identificador de tabla de la tabla temporal que se creó. El autor de la llamada debe contener código que cierre la tabla.

**cRecord**

Número de registros de la tabla temporal que se creó.

**columnidcontainername**

Identificador de columna del nombre del tipo de contenedor.

Los únicos contenedores que se admiten actualmente son tablas. Esta columna es una [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Identificador de columna del nombre del objeto.

Esta columna es una [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

Identificador de columna del tipo del objeto. Los únicos contenedores que se admiten actualmente son tablas, por lo que este campo se JET_objtypTable.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsoleto. No debe usarse.

**columniddtUpdate**

Obsoleto. No debe usarse.

**columnidgrbit**

Identificador de columna de **los bits grbits** que son aplicables al objeto . Para obtener una lista de **los bits grbits aplicables,** [vea JET_TABLECREATE](./jet-tablecreate-structure.md).

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

Identificador de columna de las marcas que son aplicables al objeto . Para obtener una lista de marcas aplicables, [vea JET_OBJECTINFO](./jet-objectinfo-structure.md).

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

Identificador de columna del número de registros presentes en la tabla denominada **columnidobjectname**.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificador de columna del número de páginas que usa el objeto.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Observaciones

Cada fila de la tabla temporal corresponde a un objeto de la base de datos.

Cuando se crea la tabla temporal con el parámetro *InfoLevel* en la función [JetGetObjectInfo](./jetgetobjectinfo-function.md) establecida en JET_ObjInfoListNoStats, las columnas identificadas por **columnidcRecord** y **columnidcPage** no contendrán información significativa.

Actualmente, solo la información sobre las tablas estará en la tabla temporal.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



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
