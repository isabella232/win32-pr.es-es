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
ms.openlocfilehash: 6ac89a45e37631b554fc7b2dc28266c95cfae3fba54debb427abfd8db621ea3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766093"
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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Códigos de error</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>El identificador de columna está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el identificador de columna no existe en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Todos los valores de esta columna son NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>JET_bitEnumeratePresenceOnly se especificó y se habría devuelto al menos un valor de columna distinto de NULL para esta columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput se especificó y se ha devuelto exactamente un valor de columna distinto de NULL para esta columna. Como resultado, se ha devuelto la <strong>forma comprimida JET_ENUMCOLUMN</strong> . Consulte <strong>JET_ENUMCOLUMN</strong> para obtener más información.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>El identificador de columna del <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> estructura correspondiente a este <strong>JET_ENUMCOLUMN</strong> estructura era cero.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matriz de valores de columna que se enumeraron para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err \! = JET_wrnColumnSingleValue".

**cbData**

Valor de columna enumerado para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna se JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

**pvData**

Valor de columna enumerado para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna se JET_wrnColumnSingleValue. Para obtener más información, [vea JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "err == JET_wrnColumnSingleValue".

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
