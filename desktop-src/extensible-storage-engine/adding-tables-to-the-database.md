---
description: 'Más información sobre: Agregar tablas a la base de datos'
title: Agregar tablas a la base de datos
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 47cb3b87b96e8cb51f651bf7c069088df9d13f7502e24ed61d9d5c355bc6d827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117903542"
---
# <a name="adding-tables-to-the-database"></a>Agregar tablas a la base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="adding-tables-to-the-database"></a>Agregar tablas a la base de datos

Las tablas son una colección heterogéneo de registros que agrupan física y lógicamente los datos de la base de datos. Las tablas se identifican de forma única por su nombre. El identificador de[tabla (JET_TABLEID](./jet-tableid.md)) es un identificador de un cursor que se usa para actualizar y navegar por las tablas. Puede abrir varias [JET_TABLEID](./jet-tableid.md) en la misma tabla.

Se abre una tabla existente en la llamada a [JetOpenTable](./jetopentable-function.md)y se crea una nueva tabla sin filas ni columnas [con JetCreateTable.](./jetcreatetable-function.md) Para crear de forma atómica una tabla con un conjunto inicial de columnas e índices, llame a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md) El tamaño inicial de la tabla se especifica en el parámetro *lPages* de [JetCreateTable](./jetcreatetable-function.md) o en el **miembro ulPages** de la estructura JET_TABLECREATE en la llamada [a](./jet-tablecreate-structure.md) [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Las tablas crecen automáticamente cuando se agregan datos a la tabla. El crecimiento es proporcional al tamaño inicial de la tabla. Las columnas se pueden agregar a la tabla en cualquier momento [con JetAddColumn](./jetaddcolumn-function.md). Cuando la aplicación ya no necesite acceder a la tabla, el cursor se puede cerrar [con JetCloseTable.](./jetclosetable-function.md) La tabla se puede eliminar mediante una llamada a [JetDeleteTable](./jetdeletetable-function.md).

Las operaciones de tabla deben realizarse en el contexto de una transacción.

## <a name="see-also"></a>Consulte también

[Transactions](./transactions.md)
