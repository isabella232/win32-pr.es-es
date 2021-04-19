---
description: 'Más información acerca de: estructura de JET_THREADSTATS'
title: Estructura de JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706894"
---
# <a name="jet_threadstats-structure"></a>Estructura de JET_THREADSTATS


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>Estructura de JET_THREADSTATS

La estructura **JET_THREADSTATS** contiene estadísticas acumuladas sobre el trabajo realizado por el motor de base de datos en el subproceso actual. Esta información se devuelve a través de [JetGetThreadStats](./jetgetthreadstats-function.md).

**Windows Vista:**  La estructura de **JET_THREADSTATS** se introduce en Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura de **JET_THREADSTATS** devuelta, en bytes.

**Nota:**  La estructura de **JET_THREADSTATS** se expandirá en el futuro para que contenga más estadísticas. Las nuevas estadísticas se agregarán al final de la estructura y se pueden recuperar con un mayor tamaño del búfer de salida. La presencia de estadísticas adicionales se puede inferir con un valor de **cbStruct** mayor.

**cPageReferenced**

Número total de páginas de base de datos visitadas por el motor de base de datos en el subproceso actual.

**cPageRead**

Número total de páginas de base de datos capturadas desde el disco por el motor de base de datos en el subproceso actual.

**cPagePreread**

Número total de páginas de base de datos capturadas previamente desde el disco por el motor de base de datos en el subproceso actual.

**cPageDirtied**

El número total de páginas de base de datos, sin cambios no escritos, modificados por el motor de base de datos en el subproceso actual.

**cPageRedirtied**

El número total de páginas de base de datos, con cambios sin escribir, modificados por el motor de base de datos en el subproceso actual.

**cLogRecord**

Número total de entradas del registro de transacciones generadas por el motor de base de datos en el subproceso actual.

**cbLogRecord**

Tamaño total en bytes de las entradas del registro de transacciones generadas por el motor de base de datos en el subproceso actual.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetGetThreadStats](./jetgetthreadstats-function.md)
