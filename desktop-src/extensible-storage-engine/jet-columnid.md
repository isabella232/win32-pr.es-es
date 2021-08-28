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
ms.openlocfilehash: d898a5943b5b80e738a331971595995d0fdee4eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482301"
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

### <a name="remarks"></a>Comentarios

Los identificadores de columna son únicos dentro de una sola tabla. Una vez que se sabe que una columna tiene un identificador de columna determinado, siempre tendrá ese identificador de columna. La restauración a partir de la copia de seguridad no cambiará el valor de un identificador de columna. Sin embargo, si se eliminan una o varias columnas de tabla, antes de una columna de tabla específica, una base de datos compacta puede cambiar el valor de un identificador de columna.

En algunos casos, los identificadores de columna son el único medio de identificar columnas. Cuando se crea una tabla temporal, sus columnas no tienen nombres, pero la función create devuelve una matriz de id. de columna.

Las columnas de tablas diferentes pueden tener el mismo identificador de columna.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


