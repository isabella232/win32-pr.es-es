---
description: 'Más información sobre: Lectura de datos de la base de datos'
title: Leer datos de la base de datos
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780265"
---
# <a name="reading-data-from-the-database"></a>Leer datos de la base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="reading-data-from-the-database"></a>Leer datos de la base de datos

La lectura de datos de la base de datos debe realizarse dentro de una transacción.

En el procedimiento siguiente se muestra cómo realizar una operación de lectura simple en la base de datos.

### <a name="to-read-data-from-a-database"></a>Para leer datos de una base de datos

1.  Llame [a JetBeginTransaction](./jetbegintransaction-function.md) o [JetBeginTransaction2](./jetbegintransaction2-function.md) con el identificador de sesión para iniciar la transacción.

2.  Mueva el cursor al registro deseado llamando a [JetMove](./jetmove-function.md) con JET_MoveFirst en el *parámetro cRow.* Para obtener más información sobre cómo mover el cursor, vea el [tema Indexación en la tabla](./indexing-in-the-table.md) .

3.  Llame [a JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) en el registro actual con JET_ColInfo especificado en el *parámetro InfoLevel* para recuperar el identificador de columna de la columna. El identificador de columna se devuelve en la [estructura JET_COLUMNDEF](./jet-columndef-structure.md) columna.

4.  Lea los datos de la columna llamando a [JetRetrieveColumn](./jetretrievecolumn-function.md) con el identificador de columna recuperado en el paso 3 del parámetro columnid. El *parámetro pvData* contiene el tipo de datos especificado en la [estructura JET_COLUMNDEF](./jet-columndef-structure.md) recuperada en el paso 3.

5.  Llame [a JetCommitTransaction](./jetcommittransaction-function.md) para confirmar la transacción en la base de datos.
