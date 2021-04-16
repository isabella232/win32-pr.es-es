---
description: 'Más información acerca de: estructura de JET_CONDITIONALCOLUMN'
title: Estructura de JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687058"
---
# <a name="jet_conditionalcolumn-structure"></a>Estructura de JET_CONDITIONALCOLUMN


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>Estructura de JET_CONDITIONALCOLUMN

La estructura **JET_CONDITIONALCOLUMN** define cómo se realiza la indización condicional para un índice determinado. Un índice condicional solo contiene una entrada de índice para las filas que coincidan con la condición especificada. Sin embargo, la columna condicional no forma parte de la clave del índice, sino que solo controla la presencia de la entrada de índice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Miembros

**cbStruct**

Este campo debe inicializarse en sizeof (JET_CONDITIONALCOLUMN), en bytes.

**szColumnName**

Nombre de la columna que contiene los datos en los que el motor de base de datos está indizando condicionalmente la fila.

**grbit** Grupo de bits que proporciona las opciones para el índice condicional. No es válido pasar valores de cero o lógicamente **o** de ed para **JET_CONDITIONALCOLUMN**. El campo de bits debe ser exactamente uno de los siguientes:

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
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>La columna especificada por el parámetro <em>szColumnName</em> debe ser null para que una entrada de índice de una fila determinada aparezca en este índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>La columna especificada por el parámetro <em>szColumnName</em> no debe ser null para una entrada de índice para que una fila determinada aparezca en este índice.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Observaciones

Un índice condicional solo contiene una entrada de índice para las filas que coincidan con la condición especificada. Por ejemplo, una columna podría denominarse "marcada" y, cuando se marca una fila, la columna se establece en un valor distinto de NULL. Un JET_bitIndexColumnMustBeNonNull índice condicional en esta columna mostrará todas las filas marcadas y un JET_bitIndexColumnMustBeNull índice condicional mostrará las filas que no están marcadas. Esta es también una manera cómoda de realizar una eliminación de marca y un índice de recolección de elementos no utilizados.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) y <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
