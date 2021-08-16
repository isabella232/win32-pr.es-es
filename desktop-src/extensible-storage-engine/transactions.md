---
description: 'Más información sobre: Transacciones (Windows eventos)'
title: Transacciones (eventos de Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e223c95d7f8af5a4350786891d58b72c508443e459990d413d5b46bc2e12a2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107060"
---
# <a name="transactions-windows-events"></a>Transacciones (eventos de Windows)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="transactions"></a>Transacciones

Las transacciones ESE son unidades lógicas de procesamiento que controlan cómo una aplicación ve y manipula filas en la base de datos. La aplicación puede usar puntos de guardado de transacciones para determinar si se debe mantener o descartar un conjunto determinado de cambios en la base de datos. Todas las transacciones de ESE son atómicas, coherentes, aisladas y duraderas (ACID), como se describe a continuación:

  - **Atomic:** Todas las actualizaciones de la transacción aparecen en la base de datos o se descartan.

<!-- end list -->

  - **Coherente:** La base de datos siempre se iniciará en un estado legal y siempre terminará en otro estado legal. Para las aplicaciones ese, el motor de base de datos controlará algunas restricciones simples, por ejemplo, la unidad de un índice único, pero la propia aplicación definirá casi todos los demás aspectos de lo que significa que la base de datos esté en un estado legal.

<!-- end list -->

  - **Aislamiento:** Las transacciones están aisladas de las actualizaciones de otras sesiones. Una transacción nunca verá un conjunto parcial de cambios realizados por otra transacción.

<!-- end list -->

  - **Durable:** Una vez que el motor de base de datos confirma que se ha confirmado una transacción, sus cambios son persistentes en la base de datos. La durabilidad de una transacción se puede suspender opcionalmente por motivos de rendimiento.

Las transacciones se realizan dentro de los límites de las llamadas a [JetBeginTransaction](./jetbegintransaction-function.md) y [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Cuando la aplicación entra en la transacción, la base de datos aparece inmovilizada en la instancia en el momento en que comienza la transacción. Esto se denomina aislamiento de instantánea. Si la transacción finaliza llamando a [JetRollback,](./jetrollback-function.md)ninguna de las operaciones realizadas en la transacción se confirma en la base de datos. Si el proceso o la máquina se bloquea antes de llamar a [JetCommitTransaction,](./jetcommittransaction-function.md) es lo mismo que llamar a [JetRollback.](./jetrollback-function.md)

Este procedimiento muestra cómo iniciar y confirmar una transacción que lee y actualiza datos en una base de datos.

### <a name="to-start-and-commit-a-transaction"></a>Para iniciar y confirmar una transacción

1.  Llame [a JetBeginTransaction](./jetbegintransaction-function.md) o [JetBeginTransaction2](./jetbegintransaction2-function.md) con el identificador de sesión para iniciar la transacción.

2.  Mueva el cursor al registro deseado llamando a [JetMove](./jetmove-function.md) con JET_MoveFirst especificado en el *parámetro cRow.* Para obtener más información sobre cómo mover el cursor, vea el [tema Indexación en la tabla](./indexing-in-the-table.md) .

3.  Llame [a JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) en el registro actual JET_ColInfo especificado en el *parámetro InfoLevel* para recuperar el identificador de columna de la columna. El identificador de columna se devuelve en la [JET_COLUMNDEF](./jet-columndef-structure.md) columna.

4.  Llame [a JetSetColumn](./jetsetcolumn-function.md) con el identificador de sesión, el identificador de tabla y el identificador de columna de la columna que se actualiza. Los datos de columna están contenidos en el *parámetro pvData.*

5.  Llame [a JetCommitTransaction](./jetcommittransaction-function.md) para confirmar la transacción en la base de datos.

La forma en que un motor de base de datos ese implementa el aislamiento de instantáneas tiene algunas diferencias importantes con respecto a los modelos tradicionales de bloqueo y aislamiento de bases de datos relacionales. Cuando una transacción lee una fila, siempre puede tener acceso a la fila sin errores o esperando a que otras sesiones liberen un bloqueo. Cuando una transacción intenta actualizar una fila, se realizará correctamente si es la primera sesión en actualizar esa fila, que es el primer escritor que gana. Si la sesión no es el primer escritor, se producirá un error de conflicto de escritura inmediatamente. A continuación, la sesión debe anular su transacción, esperar (normalmente a través de un retraso aleatorio) para que la otra transacción confirme sus cambios y, a continuación, reintentar la transacción. El motor de base de datos no hará que esa sesión espere automáticamente hasta que la otra transacción haya finalizado su actualización. Normalmente, una transacción probará si puede actualizar una fila dentro de la [llamada a JetUpdate.](./jetupdate-function.md) Si no puede bloquear la fila para la actualización, [JetUpdate](./jetupdate-function.md) producirá un error JET_errWriteConflict.

Las sesiones se limitan a un subproceso desde el momento en que se inicia la transacción hasta el final de la transacción. Se recomienda que todas las operaciones de actualización y recuperación se realicen en una transacción. ESE también admite modificaciones de esquema, como la creación de tablas y la adición de columnas dentro de la transacción. Tanto las modificaciones de actualización como de esquema se pueden realizar en la misma transacción. Una vez completada la transacción [con JetCommitTransaction,](./jetcommittransaction-function.md)la actualización se registra en el archivo de registro de transacciones. Estos archivos se pueden usar para mantener un estado coherente lógicamente en caso de una finalización inesperada del proceso o un cierre del sistema.

Las transacciones se pueden anidar hasta 7 niveles con llamadas correspondientes a [JetBeginTransaction](./jetbegintransaction-function.md) y [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) anidados entre sí. Esto permite a la aplicación revertir una parte de la transacción sin tener que salir de toda la transacción. La llamada anidada a [JetCommitTransaction](./jetcommittransaction-function.md) significa que este nivel de procesamiento está completo; sin embargo, la transacción no se confirma en la base de datos hasta que la mayoría de las llamadas externas confirmen la transacción [con JetCommitTransaction](./jetcommittransaction-function.md).

Varias sesiones pueden actualizar simultáneamente las columnas de actualización de custodia sin que se Jet_errWriteConflict. Solo se puede llamar a la función [JetEscrowUpdate](./jetescrowupdate-function.md) en columnas de custodia, columnas que se crearon con Jet_bitColumnEscrowUpdate.
