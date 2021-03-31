---
description: 'Más información acerca de: transacciones (eventos de Windows)'
title: Transacciones (eventos de Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 90b5b566f5ff961ce7b0ae3725f580e1f39c041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360990"
---
# <a name="transactions-windows-events"></a>Transacciones (eventos de Windows)


_**Se aplica a:** Windows | Windows Server_

## <a name="transactions"></a>Transacciones

Las transacciones de ESE son unidades lógicas de procesamiento que controlan el modo en que una aplicación ve y manipula filas en la base de datos. La aplicación puede utilizar puntos de almacenamiento de transacciones para determinar si se debe mantener o descartar un conjunto determinado de cambios en la base de datos. Todas las transacciones de ESE son atómicas, coherentes, aisladas y duraderas (ACID) tal y como se describe a continuación:

  - **Atómico:** Todas las actualizaciones de la transacción aparecen en la base de datos o se descartan.

<!-- end list -->

  - **Coherente:** La base de datos siempre se iniciará en un estado legal y siempre finalizará en otro estado legal. En el caso de las aplicaciones de ESE, el motor de base de datos controlará algunas restricciones simples, por ejemplo la unicidad de un índice único, pero la propia aplicación definirá casi todos los demás aspectos de lo que significa que la base de datos esté en un estado legal.

<!-- end list -->

  - **Aislamiento:** Las transacciones están aisladas de las actualizaciones realizadas por otras sesiones. Una transacción nunca verá un conjunto parcial de cambios realizados por otra transacción.

<!-- end list -->

  - **Duradero:** Una vez que el motor de base de datos confirma que se ha confirmado una transacción, sus cambios son persistentes en la base de datos. La durabilidad de una transacción se puede eximir opcionalmente por motivos de rendimiento.

Las transacciones se realizan dentro de los límites de las llamadas a [JetBeginTransaction](./jetbegintransaction-function.md) y [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md). Cuando la aplicación entra en la transacción, la base de datos aparece inmovilizada en la instancia de en el momento en que comienza la transacción. Esto se denomina aislamiento de instantánea. Si la transacción se termina llamando a [JetRollback](./jetrollback-function.md), ninguna de las operaciones realizadas en la transacción se confirma en la base de datos. Si el proceso o el equipo se bloquea antes de que se llame a [JetCommitTransaction](./jetcommittransaction-function.md) , es lo mismo que llamar a [JetRollback](./jetrollback-function.md).

Este procedimiento muestra cómo iniciar y confirmar una transacción que lee y actualiza datos en una base de datos de.

### <a name="to-start-and-commit-a-transaction"></a>Para iniciar y confirmar una transacción

1.  Llame a [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con el identificador de sesión para iniciar la transacción.

2.  Mueva el cursor al registro deseado llamando a [JetMove](./jetmove-function.md) con JET_MoveFirst especificado en el parámetro *cRow* . Para obtener más información acerca de cómo se mueve el cursor, vea el tema [indexación en la tabla](./indexing-in-the-table.md) .

3.  Llame a [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) en el registro actual con JET_ColInfo especificado en el parámetro *InfoLevel* para recuperar el ID. de columna de la columna. El ID. de columna se devuelve en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Llame a [JetSetColumn](./jetsetcolumn-function.md) con el identificador de sesión, el identificador de tabla y el identificador de columna de la columna que se actualiza. Los datos de columna se incluyen en el parámetro *pvData* .

5.  Llame a [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar la transacción en la base de datos.

La forma en que un motor de base de datos ESE implementa el aislamiento de instantáneas tiene algunas diferencias importantes con respecto a los modelos tradicionales de aislamiento y aislamiento de bases de datos relacionales. Cuando una transacción Lee una fila, siempre puede tener acceso a la fila sin errores o esperando a que otras sesiones liberen un bloqueo. Cuando una transacción intenta actualizar una fila, se realizará correctamente si es la primera sesión para actualizar esa fila, es decir, el primer escritor gana. Si la sesión no es el primer escritor, se producirá un error inmediatamente con un conflicto de escritura. A continuación, la sesión debe anular su transacción, esperar (normalmente a través de un retraso aleatorio) para que la otra transacción confirme sus cambios y, a continuación, vuelva a intentar la transacción. El motor de base de datos no hará que dicha sesión espere hasta que la otra transacción haya finalizado la actualización. Normalmente, una transacción probará si puede actualizar una fila dentro de la llamada a [JetUpdate](./jetupdate-function.md) . Si no puede bloquear la fila para la actualización, se producirá un error en [JetUpdate](./jetupdate-function.md) con JET_errWriteConflict.

Las sesiones se limitan a un subproceso desde el momento en que la transacción comienza hasta el final de la transacción. Se recomienda que todas las operaciones de actualización y recuperación se realicen en una transacción. ESE también admite modificaciones de esquema, como la creación de tablas y la adición de columnas dentro de la transacción. Las modificaciones de la actualización y del esquema se pueden realizar en la misma transacción. Una vez completada la transacción con [JetCommitTransaction](./jetcommittransaction-function.md), la actualización se registra en el archivo de registro de transacciones. Estos archivos se pueden usar para mantener un estado coherente lógicamente en caso de que se produzca una terminación inesperada de un proceso o un cierre del sistema.

Las transacciones se pueden anidar hasta 7 niveles con llamadas coincidentes a [JetBeginTransaction](./jetbegintransaction-function.md) y [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) anidadas entre sí. Esto permite que la aplicación revierta una parte de la transacción sin tener que volver a la transacción completa. La llamada anidada a [JetCommitTransaction](./jetcommittransaction-function.md) significa que se ha completado este nivel de procesamiento; sin embargo, la transacción no se confirma en la base de datos hasta la llamada más externa para confirmar la transacción con [JetCommitTransaction](./jetcommittransaction-function.md).

Las columnas de actualización de custodia se pueden actualizar simultáneamente en varias sesiones sin que se produzcan errores Jet_errWriteConflict. Solo se puede llamar a la función [JetEscrowUpdate](./jetescrowupdate-function.md) en las columnas de custodia, las columnas que se crearon con Jet_bitColumnEscrowUpdate.
