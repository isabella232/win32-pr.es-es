---
description: Más información acerca de cómo agregar tablas a la base de datos
title: Agregar tablas a la base de datos
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000879"
---
# <a name="adding-tables-to-the-database"></a>Agregar tablas a la base de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="adding-tables-to-the-database"></a>Agregar tablas a la base de datos

Las tablas son una colección heterogénea de registros que agrupan de forma física y lógica los datos en la base de datos. Las tablas se identifican de forma exclusiva por su nombre. El identificador de tabla ([JET_TABLEID](./jet-tableid.md)) es un identificador de un cursor que se utiliza para actualizar y navegar por las tablas. Puede abrir varios [JET_TABLEID](./jet-tableid.md) en la misma tabla.

Se abre una tabla existente en la llamada a [JetOpenTable](./jetopentable-function.md)y se crea una nueva tabla sin filas ni columnas con [JetCreateTable](./jetcreatetable-function.md). Para crear de forma atómica una tabla con un conjunto inicial de columnas e índices, llame a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). El tamaño inicial de la tabla se proporciona en el parámetro *lPages* de [JetCreateTable](./jetcreatetable-function.md) o en el miembro **ulPages** de la estructura [JET_TABLECREATE](./jet-tablecreate-structure.md) en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Las tablas aumentan automáticamente cuando se agregan datos a la tabla. El crecimiento es proporcional al tamaño inicial de la tabla. Se pueden agregar columnas a la tabla en cualquier momento con [JetAddColumn](./jetaddcolumn-function.md). Cuando la aplicación ya no necesita tener acceso a la tabla, el cursor se puede cerrar con [JetCloseTable](./jetclosetable-function.md). La tabla se puede eliminar mediante una llamada a [JetDeleteTable](./jetdeletetable-function.md).

Las operaciones de tabla deben realizarse en el contexto de una transacción.

## <a name="see-also"></a>Consulte también

[Transactions](./transactions.md)
