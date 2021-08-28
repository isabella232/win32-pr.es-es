---
description: 'Más información sobre: JET_COLUMNID'
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
ms.openlocfilehash: fbdc03342187cfc2adfa1dcd3ed650f532e1dbc0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982948"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_columnid"></a>JET_COLUMNID

El **JET_COLUMNID** de datos identifica una columna dentro de una tabla.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipo de datos

JET_COLUMNID

Identifica una columna dentro de una tabla.

### <a name="remarks"></a>Observaciones

Los identificadores de columna son únicos dentro de una sola tabla. Una vez que se sabe que una columna tiene un identificador de columna determinado, siempre tendrá ese identificador de columna. La restauración a partir de la copia de seguridad no cambiará el valor de un identificador de columna. Sin embargo, si se eliminan una o varias columnas de tabla, antes de una columna de tabla específica, una base de datos compacta puede cambiar el valor de un identificador de columna.

En algunos casos, los identificadores de columna son el único medio de identificar columnas. Cuando se crea una tabla temporal, sus columnas no tienen nombres, pero la función create devuelve una matriz de id. de columna.

Las columnas de tablas diferentes pueden tener el mismo identificador de columna.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


