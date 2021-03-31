---
description: 'Más información acerca de: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907647"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

El tipo de datos **JET_COLUMNID** identifica una columna dentro de una tabla.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipo de datos

JET_COLUMNID

Identifica una columna dentro de una tabla.

### <a name="remarks"></a>Observaciones

Los identificadores de columna son únicos en una sola tabla. Una vez que se sabe que una columna tiene un ID. de columna determinado, siempre tendrá ese ID. de columna. Restaurar desde copia de seguridad no cambiará el valor de un identificador de columna. Sin embargo, si se eliminan una o más columnas de la tabla, antes de una columna de tabla específica, una base de datos de Compact puede cambiar el valor de un identificador de columna.

En algunos casos, los identificadores de columna son el único medio para identificar columnas. Cuando se crea una tabla temporal, sus columnas no tienen nombres, pero la función Create devuelve una matriz de identificadores de columna.

Las columnas de tablas diferentes pueden tener el mismo ID. de columna.

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

