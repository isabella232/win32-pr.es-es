---
description: 'Más información sobre: JET_OBJECTINFO estructura'
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
ms.openlocfilehash: a24f27982285622e3b5f0893768757d27041f1c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465112"
---
# <a name="jet_objectinfo-structure"></a>Estructura de JET_OBJECTINFO


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_objectinfo-structure"></a>Estructura de JET_OBJECTINFO

La **JET_OBJECTINFO** contiene información sobre un objeto . Las tablas son los únicos tipos de objeto que se admiten actualmente.

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

Tamaño, en bytes, de la **JET_OBJECTINFO** estructura.

**objtyp**

Contiene el [JET_OBJTYP](./jet-objtyp.md) de la estructura . Actualmente solo se devolverán tablas (es decir, JET_objtypTable).

**dtCreate**

Obsoleto. No debe usarse.

**dtUpdate**

Obsoleto. No debe usarse.

**grbit**

Grupo de bits que contienen las opciones disponibles para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableInfoBookmark</p> | <p>La tabla puede tener marcadores.</p> | 
| <p>JET_bitTableInfoRollback</p> | <p>La tabla se puede revertir.</p> | 
| <p>JET_bitTableInfoUpdatable</p> | <p>La tabla se puede actualizar.</p> | 



**flags**

Campo de bits que contiene cero o más de las marcas siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitObjectSystem</p> | <p>La tabla es una tabla del sistema y es solo para uso interno.</p> | 
| <p>JET_bitObjectTableDerived</p> | <p>La tabla heredó DDL de una tabla de plantillas.</p> | 
| <p>JET_bitObjectTableFixedDDL</p> | <p>No se puede modificar el DDL de la tabla.</p> | 
| <p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p> | <p>Se usa junto con JET_bitObjectTableTemplate para no permitir columnas fijas o variables en tablas derivadas (de modo que las columnas fijas o variables se puedan agregar a la plantilla en el futuro).</p><p><strong>Windows XP:</strong> Este valor se introduce en Windows XP.</p> | 
| <p>JET_bitObjectTableTemplate</p> | <p>La tabla es una tabla de plantillas.</p> | 



**cRecord**

Número de registros de la tabla.

Este valor solo se recupera si **JET_OBJECTINFO** se pasó [a JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

Número de páginas que usa la tabla.

Este valor solo se recupera si **JET_OBJECTINFO** se pasó [a JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Comentarios

Una **JET_OBJECTINFO** estructura se rellena mediante una llamada a [JetGetObjectInfo](./jetgetobjectinfo-function.md) o [JetGetTableInfo.](./jetgettableinfo-function.md) Si la llamada API no se realiza correctamente, el contenido de la estructura es indefinido.

Si procede, las estadísticas de tabla incluyen el número de registros y el número de páginas que se encuentran en el índice clúster (es decir, el índice que contiene los datos del registro). Se accede a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



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
