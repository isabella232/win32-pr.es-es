---
description: 'Más información sobre: JET_ENUMCOLUMN estructura'
title: Estructura de JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: 4f27fd08cb9df4c9e777524b14c1dfbdfe274dab
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988648"
---
# <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN

La **JET_ENUMCOLUMN** enumera los valores de columna de un registro cuando se usa la función [JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de **JET_ENUMCOLUMN** estructuras. La matriz se devuelve en memoria que se asigna mediante la devolución de llamada compatible con [el](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a esa API.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Miembros

**columnid**

El identificador de columna que se enumeró.

**Err**

Código de estado de columna que resulta de la enumeración de la columna.


| <p>Códigos de error</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errBadColumnId</p> | <p>El identificador de columna está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el identificador de columna no existe en la tabla.</p> | 
| <p>JET_wrnColumnNull</p> | <p>Todos los valores de esta columna son NULL.</p> | 
| <p>JET_wrnColumnPresent</p> | <p>JET_bitEnumeratePresenceOnly se especificó y se habría devuelto al menos un valor de columna distinto de NULL para esta columna.</p> | 
| <p>JET_wrnColumnSingleValue</p> | <p>JET_bitEnumerateCompressOutput se especificó y se ha devuelto exactamente un valor de columna distinto de NULL para esta columna. Como resultado, se ha devuelto la <strong>forma JET_ENUMCOLUMN</strong> comprimida de . Consulte <strong>JET_ENUMCOLUMN</strong> para obtener más información.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>El identificador de columna del <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct correspondiente a este <strong>JET_ENUMCOLUMN</strong> struct era cero.</p> | 



**cEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**cbData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

**pvData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
