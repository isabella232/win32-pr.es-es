---
description: 'Más información acerca de: uso de columnas en una tabla'
title: Usar columnas en una tabla
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cd715b171162f63aaf0772ff6ec2e4a6d057a0d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715288"
---
# <a name="using-columns-in-a-table"></a>Usar columnas en una tabla


_**Se aplica a:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Usar columnas en una tabla

Se puede crear una tabla con un conjunto inicial de columnas mediante una llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o sin columnas mediante una llamada a [JetCreateTable](./jetcreatetable-function.md). Cuando la tabla se crea con un conjunto inicial de columnas en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), contiene una estructura [JET_TABLECREATE](./jet-tablecreate-structure.md) (o [JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Estas estructuras contienen una matriz de estructuras [JET_COLUMNCREATE](./jet-columncreate-structure.md) que definen el conjunto de columnas de la tabla. El miembro **grbit** establece las opciones de la columna y el miembro **coltyp** establece el tipo de datos que se pueden establecer en la columna.

Cuando se crea la tabla sin columnas, se deben agregar llamando a [JetAddColumn](./jetaddcolumn-function.md) con la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) . El miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) establece las opciones de la columna y el miembro **coltyp** establece el tipo de datos que se pueden establecer en la columna. Los valores de columna predeterminados se establecen en la llamada a [JetAddColumn](./jetaddcolumn-function.md) especificando un valor en el parámetro *pvDefault* y el tamaño en el parámetro *cbDefault* . Una columna sin un valor predeterminado tiene eficazmente un valor predeterminado de NULL.

Los valores de la tabla solo se pueden establecer en el contexto de una transacción. La transacción comienza en la llamada a [JetBeginTransaction](./jetbegintransaction-function.md) y finaliza en la llamada a [JetCommitTransaction](./jetcommittransaction-function.md). Dentro de la transacción, se puede establecer un valor de columna único mediante una llamada a [JetSetColumn](./jetsetcolumn-function.md), o bien se pueden establecer varios valores de columnas llamando a [JetSetColumns](./jetsetcolumns-function.md). [JetSetColumns](./jetsetcolumns-function.md) utiliza una matriz de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) para establecer varias columnas en la tabla. Los datos se encuentran en el parámetro *pvData* de [JetSetColumn](./jetsetcolumn-function.md)o en el miembro **pvData** de la estructura [JET_SETCOLUMN](./jet-setcolumn-structure.md) .

Las estructuras [JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)y [JET_COLUMNDEF](./jet-columndef-structure.md) se devuelven en las llamadas a [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)y [JetGetColumnInfo](./jetgetcolumninfo-function.md) según el tipo de columna que se recupera. La estructura de [JET_COLUMNBASE](./jet-columnbase-structure.md) describe los parámetros de la columna base y el [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene la información necesaria para recorrer la tabla temporal creada por las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .
