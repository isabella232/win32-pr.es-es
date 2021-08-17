---
description: 'Más información sobre: Versión, Incremento automático y Columnas de custodia'
title: Versión, incremento automático y columnas de custodia
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: b86b37663f7968ad77874ebcc7b2d0f8fd569cc265424bc36feeecccb6d7e148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471285"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Versión, incremento automático y columnas de custodia


_**Se aplica a:** Windows | Windows Servidor_

## <a name="version-auto-increment-and-escrow-columns"></a>Versión, incremento automático y columnas de custodia

ESE proporciona tipos de columna de actualización de versión, incremento automático y custodia que tienen capacidades especiales. Las opciones de columna establecidas en el miembro **grbit** de la estructura JET_COLUMNDEF utilizada en la llamada [a](./jet-columndef-structure.md) [JetAddColumn](./jetaddcolumn-function.md) indican si la columna es uno de los tipos especializados que se indican aquí.

### <a name="version-jet_bitcolumnversion"></a>Versión (JET_bitColumnVersion)

La opción de columna de versión, que se aplica solo JET_coltypLong columnas, indica que la columna contiene información de versión sobre el registro que se puede usar para determinar si es necesario actualizar una copia en memoria de un registro determinado. Las columnas de versión se incrementan automáticamente por ESE cuando la aplicación modifica la columna a través [de JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automático (JET_bitColumnAutoincrement)

Las columnas de incremento automático se incrementan automáticamente mediante ESE cuando se inserta un nuevo registro en la tabla. El valor contenido en la columna de incremento automático es único para cada registro de la tabla y no se garantiza que sea continuo. Estos valores no se reciclan, pero se pueden reutilizar en determinados casos. Solo las columnas de tipo JET_coltypLong y JET_coltypLongLong pueden ser columnas de incremento automático.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Custodia (JET_bitColumnEscrowUpdate)

Las columnas de custodia se pueden modificar en la llamada a [JetEscrowUpdate](./jetescrowupdate-function.md). Las actualizaciones en custodia son operaciones diferenciales numéricas que no sufren conflictos de escritura. Esto significa que cualquier número de sesiones puede actualizar simultáneamente una columna de custodia en un registro a través de [JetEscrowUpdate](./jetescrowupdate-function.md) sin conflictos. Tenga en cuenta que cualquier otra operación de actualización puede seguir causando un conflicto de escritura con una operación de actualización de custodia. Las actualizaciones de custodia solo se pueden realizar en columnas de tipo JET_coltypLong que tengan un valor predeterminado. Estas columnas también se deben agregar a una tabla antes de cargarse con filas. Por último, las filas que contienen una columna de actualización de custodia se pueden configurar para admitir una devolución de llamada de fin de fila (JET_bitColumnFinalize) o para eliminarse automáticamente si el recuento de referencias alcanza cero (JET_bitColumnDeleteOnZero). Para obtener más información, vea la [estructura JET_COLUMNDEF](./jet-columndef-structure.md) datos.
