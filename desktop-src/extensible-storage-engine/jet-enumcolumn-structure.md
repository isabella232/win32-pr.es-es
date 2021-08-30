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
ms.openlocfilehash: 7f0fa6d326120355e43b29cd87e13d5c0ebbf68b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474541"
---
# <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN

La **JET_ENUMCOLUMN** enumera los valores de columna de un registro cuando se usa la función [JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de **JET_ENUMCOLUMN** estructuras. La matriz se devuelve en memoria que se asigna mediante la [devolución](/cpp/c-runtime-library/reference/realloc?view=vs-2019) de llamada compatible con reasignación que se proporcionó a esa API.

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

Identificador de columna enumerado.

**Err**

Código de estado de columna que resulta de la enumeración de la columna.


| <p>Códigos de error</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errBadColumnId</p> | <p>El identificador de columna está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el identificador de columna no existe en la tabla.</p> | 
| <p>JET_wrnColumnNull</p> | <p>Todos los valores de esta columna son NULL.</p> | 
| <p>JET_wrnColumnPresent</p> | <p>JET_bitEnumeratePresenceOnly se especificó y se habría devuelto al menos un valor de columna distinto de NULL para esta columna.</p> | 
| <p>JET_wrnColumnSingleValue</p> | <p>JET_bitEnumerateCompressOutput se especificó y se ha devuelto exactamente un valor de columna distinto de NULL para esta columna. Como resultado, se ha devuelto la <strong>forma comprimida JET_ENUMCOLUMN</strong> . Consulte <strong>JET_ENUMCOLUMN</strong> para obtener más información.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>El identificador de columna del <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> estructura correspondiente a esta <strong>estructura JET_ENUMCOLUMN</strong> estructura era cero.</p> | 



**cEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**cbData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna se JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

**pvData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna se JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
