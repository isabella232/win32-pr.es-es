---
description: 'Más información sobre: Usar columnas en una tabla'
title: Usar columnas en una tabla
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 332cca1c64c851ded44951fc9bb7f68ebd9f6818030cefeb8406f965a1bd5d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471305"
---
# <a name="using-columns-in-a-table"></a>Usar columnas en una tabla


_**Se aplica a:** Windows | Windows Servidor_

## <a name="using-columns-in-a-table"></a>Usar columnas en una tabla

Una tabla se puede crear con un conjunto inicial de columnas llamando a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o sin columnas llamando a [JetCreateTable](./jetcreatetable-function.md). Cuando la tabla se crea con un conjunto inicial de columnas en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2,](./jetcreatetablecolumnindex2-function.md)contiene una [estructura JET_TABLECREATE](./jet-tablecreate-structure.md) [(o JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Estas estructuras contienen una matriz de [estructuras JET_COLUMNCREATE](./jet-columncreate-structure.md) que definen el conjunto de columnas de la tabla. El **miembro grbit** establece las opciones de la columna y el miembro **coltyp** establece el tipo de datos que se pueden establecer en la columna.

Cuando la tabla se crea sin columnas, se deben agregar llamando a [JetAddColumn](./jetaddcolumn-function.md) con [la JET_COLUMNDEF](./jet-columndef-structure.md) estructura. El **miembro grbit** de la [estructura JET_COLUMNDEF](./jet-columndef-structure.md) establece las opciones de la columna y el miembro **coltyp** establece el tipo de datos que se pueden establecer en la columna. Los valores de columna predeterminados se establecen en la llamada a [JetAddColumn](./jetaddcolumn-function.md) especificando un valor en el parámetro *pvDefault* y el tamaño en el *parámetro cbDefault.* Una columna sin un valor predeterminado tiene eficazmente un valor predeterminado de NULL.

Los valores de la tabla solo se pueden establecer en el contexto de una transacción. La transacción comienza en la llamada [a JetBeginTransaction](./jetbegintransaction-function.md) y termina en la llamada a [JetCommitTransaction](./jetcommittransaction-function.md). Dentro de la transacción, se puede establecer un valor de columna única mediante una llamada a [JetSetColumn](./jetsetcolumn-function.md)o se pueden establecer varios valores de columnas llamando a [JetSetColumns](./jetsetcolumns-function.md). [JetSetColumns](./jetsetcolumns-function.md) usa una matriz de [estructuras JET_SETCOLUMN](./jet-setcolumn-structure.md) para establecer varias columnas en la tabla. Los datos están contenidos en el *parámetro pvData* de [JetSetColumn](./jetsetcolumn-function.md)o en el **miembro pvData** [de JET_SETCOLUMN](./jet-setcolumn-structure.md) estructura.

Las [JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)y JET_COLUMNDEF se devuelven en las llamadas [a](./jet-columndef-structure.md) [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)y [JetGetColumnInfo](./jetgetcolumninfo-function.md) en función del tipo de columna que se recupere. La [JET_COLUMNBASE](./jet-columnbase-structure.md) describe los parámetros de la columna base y el [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene la información necesaria para recorrer la tabla temporal creada por las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)
