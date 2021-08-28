---
description: 'Más información sobre: JET_RETINFO estructura'
title: JET_RETINFO estructura
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
ms.openlocfilehash: 3ddf6f7b2ef129ab620a61616d975c8b8470022e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470791"
---
# <a name="jet_retinfo-structure"></a>JET_RETINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_retinfo-structure"></a>JET_RETINFO estructura

La **JET_RETINFO** estructura contiene parámetros de entrada y salida opcionales [para JetRetrieveColumn](./jetretrievecolumn-function.md). Se puede pasar un puntero nulo donde, de lo contrario, se pasaría un puntero a esta estructura. Pasar un puntero nulo es lo mismo que pasar **JET_RETINFO** con **cbStruct** establecido en sizeof(JET_RETINFO), **ibLongValue** establecido en 0 (cero) e **itagSequence** establecido en 1.

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

Debe establecerse en el tamaño de la **estructura JET_RETINFO,** en bytes, y sirve para confirmar la presencia de los campos siguientes.

**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de [tipo JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md). Tenga en cuenta que la cantidad de datos recuperados de este desplazamiento es la menor del tamaño del búfer de salida y el tamaño de los datos en el valor real después de este desplazamiento.

**itagSequence**

Describe el número de secuencia del valor de una columna con varios valores. Tenga en cuenta que la matriz de valores está basada en uno. El primer valor es la secuencia 1, no 0. Si la columna de registro solo tiene un valor, se debe pasar 1 como **itagSequence.**

Con una columna que puede contener varios valores, solo es posible usar un número de secuencia mayor que 1 en [JetSetColumn](./jetsetcolumn-function.md) y [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 en [JetSetColumn.](./jetsetcolumn-function.md) En la implementación actual del motor, cualquier columna que se creó con JET_bitColumnTagged puede contener varios valores. Las columnas creadas con JET_bitColumnMultiValued difieren de las columnas etiquetadas con varios valores solo en la forma en que se indexan. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información.

**columnidNextTagged**

Devuelve el columnid de la columna etiquetada, multivalor o dispersa recuperada cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid a [JetRetrieveColumn.](./jetretrievecolumn-function.md)

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
