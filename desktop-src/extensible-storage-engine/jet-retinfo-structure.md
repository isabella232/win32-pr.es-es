---
description: 'Más información acerca de: estructura de JET_RETINFO'
title: Estructura de JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908149"
---
# <a name="jet_retinfo-structure"></a>Estructura de JET_RETINFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>Estructura de JET_RETINFO

La estructura **JET_RETINFO** contiene parámetros de entrada y salida opcionales para [JetRetrieveColumn](./jetretrievecolumn-function.md). Se puede pasar un puntero NULL en el caso de que se pasara un puntero a esta estructura. Pasar un puntero nulo es igual que pasar **JET_RETINFO** con **cbStruct** establecido en sizeof (JET_RETINFO), **ibLongValue** establecido en 0 (cero) y **itagSequence** establecido en 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Miembros

**cbStruct**

Debe establecerse en el tamaño de la estructura **JET_RETINFO** , en bytes, y sirve para confirmar la presencia de los campos siguientes.

**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md), o [JET_coltypLongText](./jet-coltyp.md). Observe que la cantidad de datos recuperados de este desplazamiento es el menor del tamaño del búfer de salida y el tamaño de los datos en el valor real después de este desplazamiento.

**itagSequence**

Describe el número de secuencia de un valor en una columna con varios valores. Tenga en cuenta que la matriz de valores se basa en uno. El primer valor es Sequence 1, no 0. Si la columna de registro solo tiene un valor, se debe pasar 1 como **itagSequence**

Con una columna que puede contener varios valores, solo es posible usar un número de secuencia mayor que 1 en [JetSetColumn](./jetsetcolumn-function.md) y [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 en [JetSetColumn](./jetsetcolumn-function.md). En la implementación actual del motor, cualquier columna creada con JET_bitColumnTagged puede contener varios valores. Las columnas creadas con JET_bitColumnMultiValued solo se diferencian de las columnas etiquetadas con varios valores en la forma en que se indexan. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información.

**columnidNextTagged**

Devuelve el columnid de la columna etiquetada, con varios valores o dispersos recuperados cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid a [JetRetrieveColumn](./jetretrievecolumn-function.md).

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
