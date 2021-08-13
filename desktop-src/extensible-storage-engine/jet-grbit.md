---
description: 'Más información sobre: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 2b54ed8a95d81c148b68727384dd76fba3d2dc8b1f9d6452c2105bc45f015646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362285"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_grbit"></a>JET_GRBIT

El **JET_GRBIT** de datos es un grupo de bits que contienen constantes que son específicas de las funciones y estructuras en las que se usa.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipo de datos

JET_GRBIT

En general, las constantes que se usan como valores para este tipo de datos reflejan el nombre del elemento de API en el que se usan. Por ejemplo, todas las constantes que se pasan [a JetRetrieveColumn](./jetretrievecolumn-function.md) comienzan por "JET_bitRetrieve". De forma similar, todas las constantes que se pasan [a JetSetColumn](./jetsetcolumn-function.md) comienzan por "JET_bitSet".

Un valor de cero hace que se ignore el parámetro.

### <a name="remarks"></a>Comentarios

Para obtener más información, vea la función o estructura específica. Las opciones normalmente se pasan como un conjunto de marcas que se pueden combinar.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
