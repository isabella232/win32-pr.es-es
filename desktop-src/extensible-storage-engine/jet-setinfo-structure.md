---
description: 'Más información sobre: JET_SETINFO estructura'
title: JET_SETINFO estructura
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 379fd60a001312152dbe181c27a3e8158ceca79b4cfa9075a530b6c73f4337cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253446"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_setinfo-structure"></a>JET_SETINFO estructura

La **JET_SETINFO** contiene parámetros de entrada opcionales [para JetSetColumn.](./jetsetcolumn-function.md) Se **puede pasar** un puntero NULL donde, de lo contrario, se pasaría un puntero a esta estructura. El significado de pasar un **valor NULL** es el mismo que pasar **JET_SETINFO** con **cbStruct** establecido en sizeof(JET_SETINFO), **ibLongValue** establecido en 0 (cero) e **itagSequence** establecido en 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, del **JET_SETINFO**. Este valor confirma la presencia de los campos siguientes.

**ibLongValue**

Desplazamiento al primer byte que se va a establecer en una columna de [tipo JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Describe el número de secuencia del valor de una columna de varios valores que se va a establecer. La matriz de valores se basa en uno. El primer valor es la secuencia 1, no 0 (cero). Si la columna de registro solo tiene un valor, se debe pasar 1 como **itagSequence** si ese valor se va a reemplazar. Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.

Con una columna que puede contener varios valores, solo es posible usar un número de secuencia mayor que 1 en [JetSetColumn](./jetsetcolumn-function.md) y [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 en [JetSetColumn.](./jetsetcolumn-function.md) En la implementación actual del motor, cualquier columna que se creó con JET_bitColumnTagged puede contener varios valores. Las columnas creadas con JET_bitColumnMultiValued difieren de las columnas etiquetadas con varios valores solo en la forma en que se indexan. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información.

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
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetSetColumn](./jetsetcolumn-function.md)
