---
description: 'Más información acerca de: estructura de JET_RECPOS'
title: Estructura de JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716515"
---
# <a name="jet_recpos-structure"></a>Estructura de JET_RECPOS


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>Estructura de JET_RECPOS

La estructura **JET_RECPOS** contiene una colección de enteros que representan una posición fraccionaria dentro de un índice. **centriesLT** es el número de entradas de índice menor que la clave de índice actual. **centriesInRange** es el número de entradas de índice igual a la clave actual. **centriesInRange** no se admite y siempre se devuelve como 1. **centriesTotal** es el número de entradas de índice en el índice. Todos los valores son aproximaciones sin ninguna garantía de precisión.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura de [JET_RETINFO](./jet-retinfo-structure.md) , en bytes. Este valor confirma la presencia de los campos siguientes.

**centriesLT**

Número aproximado de entradas de índice que son menores que la clave actual.

**centriesInRange**

El número aproximado de entradas de índice igual a la clave actual. Este campo siempre se establece en 1, independientemente del número de entradas de índice que sean realmente iguales a la clave actual.

**centriesTotal**

Número aproximado de entradas en el índice.

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
