---
description: 'Más información sobre: JET_THREADSTATS estructura'
title: JET_THREADSTATS estructura
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
ms.openlocfilehash: 7f94c9911fb7ab974f87cfed41e92b53ac0a66cb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983568"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS estructura

La **JET_THREADSTATS** contiene estadísticas acumulativas sobre el trabajo realizado por el motor de base de datos en el subproceso actual. Esta información se devuelve a [través de JetGetThreadStats.](./jetgetthreadstats-function.md)

**Windows Vista:**  La **JET_THREADSTATS** estructura se introduce en Windows Vista.

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

Tamaño de la estructura **JET_THREADSTATS,** en bytes.

**Nota**  La **JET_THREADSTATS** se expandirá en el futuro para contener más estadísticas. Se agregarán nuevas estadísticas al final de la estructura y se pueden recuperar con un mayor tamaño de búfer de salida. La presencia de estadísticas adicionales se puede inferir mediante un valor **cbStruct** mayor.

**cPageReferenced**

Número total de páginas de base de datos visitadas por el motor de base de datos en el subproceso actual.

**cPageRead**

Número total de páginas de base de datos capturadas del disco por el motor de base de datos en el subproceso actual.

**cPagePreread**

Número total de páginas de base de datos capturadas previamente desde el disco por el motor de base de datos en el subproceso actual.

**cPageDirtied**

Número total de páginas de base de datos, sin cambios no escritos, que el motor de base de datos ha modificado en el subproceso actual.

**cPageRedirtied**

Número total de páginas de base de datos, con cambios no escritos, que el motor de base de datos ha modificado en el subproceso actual.

**cLogRecord**

Número total de registros de transacciones generados por el motor de base de datos en el subproceso actual.

**cbLogRecord**

Tamaño total en bytes de registros de transacciones generados por el motor de base de datos en el subproceso actual.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetGetThreadStats](./jetgetthreadstats-function.md)
