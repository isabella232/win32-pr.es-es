---
description: 'Más información acerca de: JET_GRBIT'
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105678855"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

El tipo de datos **JET_GRBIT** es un grupo de bits que contiene constantes que son específicas de las funciones y estructuras en las que se utiliza.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipo de datos

JET_GRBIT

En general, las constantes que se usan como valores para este tipo de datos reflejan el nombre del elemento de la API en el que se usan. Por ejemplo, todas las constantes pasadas a [JetRetrieveColumn](./jetretrievecolumn-function.md) comienzan con "JET_bitRetrieve". Del mismo modo, todas las constantes pasadas a [JetSetColumn](./jetsetcolumn-function.md) comienzan con "JET_bitSet".

Un valor de cero hace que el parámetro se omita.

### <a name="remarks"></a>Observaciones

Para obtener más información, vea la función o estructura específica. Normalmente, las opciones se pasan como un conjunto de marcas que se pueden combinar.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
