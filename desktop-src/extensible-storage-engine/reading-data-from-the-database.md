---
description: Más información acerca de cómo leer datos de la base de datos
title: Leer datos de la base de datos
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687678"
---
# <a name="reading-data-from-the-database"></a>Leer datos de la base de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Leer datos de la base de datos

La lectura de datos de la base de datos debe realizarse dentro de una transacción.

En el procedimiento siguiente se muestra cómo realizar una operación de lectura simple en la base de datos.

### <a name="to-read-data-from-a-database"></a>Para leer datos de una base de datos

1.  Llame a [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con el identificador de sesión para iniciar la transacción.

2.  Mueva el cursor al registro deseado llamando a [JetMove](./jetmove-function.md) con JET_MoveFirst en el parámetro *cRow* . Para obtener más información acerca de cómo se mueve el cursor, vea el tema [indexación en la tabla](./indexing-in-the-table.md) .

3.  Llame a [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) en el registro actual con JET_ColInfo especificado en el parámetro *InfoLevel* para recuperar el ID. de columna de la columna. El ID. de columna se devuelve en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Lea los datos de la columna mediante una llamada a [JetRetrieveColumn](./jetretrievecolumn-function.md) con el identificador de columna recuperado en el paso 3 en el parámetro columnid. El parámetro *pvData* contiene el tipo de datos especificado en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) recuperada en el paso 3.

5.  Llame a [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar la transacción en la base de datos.
