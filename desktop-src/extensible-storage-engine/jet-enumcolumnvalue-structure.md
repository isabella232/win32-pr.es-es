---
description: 'Más información acerca de: estructura de JET_ENUMCOLUMNVALUE'
title: Estructura de JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697530"
---
# <a name="jet_enumcolumnvalue-structure"></a>Estructura de JET_ENUMCOLUMNVALUE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>Estructura de JET_ENUMCOLUMNVALUE

La estructura **JET_ENUMCOLUMNVALUE** enumera los valores de columna de un registro mediante la función [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de estructuras **JET_ENUMCOLUMNVALUE** . La matriz se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a esa función.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Miembros

**itagSequence**

Valor de columna (por índice de base uno) que se enumeró.

**ERR**

El código de estado de la columna resultante de la enumeración del valor de la columna.

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
<td><p>JET_wrnColumnNull</p></td>
<td><p>El valor de la columna solicitada es NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>El <em>itagSequence</em> que se especifica en el elemento de la matriz <em>rgtagSequence</em> en el <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct correspondiente a este <strong>JET_ENUMCOLUMNVALUE</strong> struct era cero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>El valor de la columna solicitada se truncó hasta el tamaño especificado antes de devolverse.</p>
<p>Este truncamiento solo se produce para las columnas de texto largo y Long Binary que contienen grandes cantidades de datos.</p></td>
</tr>
</tbody>
</table>


**cbData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

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

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
