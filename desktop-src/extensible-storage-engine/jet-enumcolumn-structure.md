---
description: 'Más información acerca de: estructura de JET_ENUMCOLUMN'
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153799"
---
# <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_enumcolumn-structure"></a>Estructura de JET_ENUMCOLUMN

La estructura **JET_ENUMCOLUMN** enumera los valores de columna de un registro cuando se usa la función [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de estructuras **JET_ENUMCOLUMN** . La matriz se devuelve en memoria que se asigna mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a esa API.

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

El ID. de columna que se enumeró.

**ERR**

El código de estado de la columna que es el resultado de la enumeración de la columna.

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
<td><p>El ID. de columna está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el ID. de columna no existe en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Todos los valores de esta columna son NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>Se especificó JET_bitEnumeratePresenceOnly y se habría devuelto al menos un valor de columna que no sea NULL para esta columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>Se especificó JET_bitEnumerateCompressOutput y se devolvió exactamente un valor de columna distinto de NULL para esta columna. Como resultado, se ha devuelto el formulario comprimido de <strong>JET_ENUMCOLUMN</strong> . Consulte <strong>JET_ENUMCOLUMN</strong> para obtener más información.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>El ID. de columna del <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct correspondiente a este <strong>JET_ENUMCOLUMN</strong> struct era cero.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Matriz de valores de columna que se enumeró para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, vea [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "Err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matriz de valores de columna que se enumeró para la columna. El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida se usa cuando el código de estado de la columna no es igual a JET_wrnColumnSingleValue. Para obtener más información, vea [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "Err \! = JET_wrnColumnSingleValue".

**cbData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna es JET_wrnColumnSingleValue. Para obtener más información, vea [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "Err = = JET_wrnColumnSingleValue".

**pvData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Este búfer de salida solo se usa cuando el código de estado de la columna es JET_wrnColumnSingleValue. Para obtener más información, vea [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Se devuelve si "Err = = JET_wrnColumnSingleValue".

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
