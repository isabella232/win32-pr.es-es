---
description: Más información acerca de las columnas versión, incremento automático y custodia
title: Columnas de versión, incremento automático y custodia
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715287"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Columnas de versión, incremento automático y custodia


_**Se aplica a:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Columnas de versión, incremento automático y custodia

ESE proporciona tipos de columna de actualización de versión, incremento automático y custodia que tienen capacidades especiales. Las opciones de columna establecidas en el miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizada en la llamada a [JetAddColumn](./jetaddcolumn-function.md) indican si la columna es uno de los tipos especializados indicados aquí.

### <a name="version-jet_bitcolumnversion"></a>Versión (JET_bitColumnVersion)

La opción de columna versión, que se aplica solo a JET_coltypLong columnas, indica que la columna contiene información de versión sobre el registro que se puede utilizar para determinar si es necesario actualizar una copia en memoria de un registro determinado. ESE incrementa automáticamente las columnas de versión cuando la aplicación modifica la columna a través de [JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automático (JET_bitColumnAutoincrement)

ESE incrementa automáticamente las columnas de incremento automático cuando se inserta un nuevo registro en la tabla. El valor contenido en la columna de incremento automático es único para cada registro de la tabla y no se garantiza que sea continuo. Estos valores no se reciclan, pero se pueden reutilizar en ciertos casos. Solo las columnas de tipo JET_coltypLong y JET_coltypLongLong pueden ser columnas de incremento automático.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Custodia (JET_bitColumnEscrowUpdate)

Las columnas de custodia se pueden modificar en la llamada a [JetEscrowUpdate](./jetescrowupdate-function.md). Las actualizaciones de custodia son operaciones de Delta numéricas que no sufren conflictos de escritura. Esto significa que cualquier número de sesiones puede actualizar simultáneamente una columna de custodia en un registro a través de [JetEscrowUpdate](./jetescrowupdate-function.md) sin conflictos. Tenga en cuenta que cualquier otra operación de actualización puede producir un conflicto de escritura con una operación de actualización de custodia. Solo se pueden realizar actualizaciones de custodia en columnas de tipo JET_coltypLong que tengan un valor predeterminado. Estas columnas también se deben agregar a una tabla antes de que se carguen con filas. Por último, las filas que contienen una columna de actualización de custodia se pueden configurar para que admitan una devolución de llamada de finalización de filas (JET_bitColumnFinalize) o que se eliminen automáticamente si el recuento de referencias llega a cero (JET_bitColumnDeleteOnZero). Para obtener más información, vea la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) .
