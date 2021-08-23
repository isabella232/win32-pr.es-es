---
description: 'Más información sobre: JET_CONDITIONALCOLUMN estructura'
title: JET_CONDITIONALCOLUMN estructura
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
ms.openlocfilehash: 870536ff408558332e6a07f91649edb1a17ca2fb0c69ed46fb7171f3505d683e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731155"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN estructura

La **JET_CONDITIONALCOLUMN** estructura define cómo se realiza la indexación condicional para un índice determinado. Un índice condicional contiene una entrada de índice solo para las filas que coinciden con la condición especificada. Sin embargo, la columna condicional no forma parte de la clave del índice, solo controla la presencia de la entrada de índice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Miembros

**cbStruct**

Este campo debe inicializarse en sizeof( JET_CONDITIONALCOLUMN ), en bytes.

**szColumnName**

Nombre de la columna que contiene los datos en los que el motor de base de datos indexa condicionalmente la fila.

**grbit** Grupo de bits que proporciona las opciones para el índice condicional. Pasar cero o valores lógicos **or** ed no es válido para **JET_CONDITIONALCOLUMN**. El campo de bits debe ser exactamente uno de los siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>La columna especificada por el <em>parámetro szColumnName</em> debe ser NULL para que una entrada de índice de una fila determinada aparezca en este índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>La columna especificada por el parámetro <em>szColumnName</em> debe ser no NULL para una entrada de índice con el fin de que una fila determinada aparezca en este índice.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Comentarios

Un índice condicional contiene una entrada de índice solo para las filas que coinciden con la condición especificada. Por ejemplo, una columna podría denominarse "Marked" y, cuando se marca una fila, la columna se establece en un valor distinto de NULL. Un JET_bitIndexColumnMustBeNonNull condicional en esta columna mostrará todas las filas marcadas y un índice condicional JET_bitIndexColumnMustBeNull mostrará las filas que no están marcadas. También es una manera cómoda de realizar una eliminación de marcas y un índice de recolección de elementos no utilizados.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) <strong>y JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
