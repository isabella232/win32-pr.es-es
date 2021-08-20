---
description: 'Más información sobre: Identificadores de ESE'
title: Identificadores de ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5177de8b7fbc07d592bb599941a1fd02810bbbf81e16b65cd15c6ebdfd75d3d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786305"
---
# <a name="ese-handles"></a>Identificadores de ESE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="ese-handles"></a>Identificadores de ESE

Los identificadores ese se usan para crear sesiones y acceder a las bases de datos. Se mantienen en una jerarquía, lo que significa que la salida de un nivel se usa para acceder a los recursos del siguiente nivel.

El diagrama aquí muestra la jerarquía de identificadores y las funciones correspondientes que crean los identificadores. También se indica junto con las funciones los identificadores que se usan en la llamada para crear el nuevo identificador.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Como se muestra en el diagrama, la instancia es el identificador raíz y el nivel en el que se recupera la base de datos en caso de una finalización inesperada del proceso o un apagado del sistema. El identificador de instancia, JET_INSTANCE, lo crean [JetCreateInstance](./jetcreateinstance-function.md) y [JetCreateInstance2.](./jetcreateinstance2-function.md) El siguiente nivel, el nivel de sesión, es el contexto de transacción del motor de base de datos y el nivel bajo el que se realizan todas las operaciones de base de datos. El identificador de sesión, JET_SESID, se crea en el contexto de la instancia de en la llamada a [JetBeginSession](./jetbeginsession-function.md). El identificador de sesión se usa en todas las llamadas posteriores para acceder a tablas y bases de datos. Si más de un subproceso utiliza la instancia a la vez, cada subproceso debe usar su propio identificador de sesión. El identificador de base de datos se crea mediante el identificador de sesión y se usa principalmente para administrar el esquema de la base de datos, pero también se puede usar para administrar tablas dentro de la base de datos. Los identificadores de base de datos solo se pueden usar en la sesión en la que se crean. El identificador de la base de datos se crea en la llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase.](./jetopendatabase-function.md) Las tablas están asociadas al identificador de base de datos con el que se crean.

El JET_TABLEID tipo de datos contiene un identificador para un cursor de base de datos. Se usa para examinar registros, buscar registros o crear registros de actualización y eliminación. El identificador de tabla se crea en la llamada a [JetOpenTable](./jetopentable-function.md)o [JetCreateTable.](./jetcreatetable-function.md) [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)y [JetOpenTempTable3](./jetopentemptable3-function.md) también crean los id. de tabla para las tablas temporales, y [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) y [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) devuelven los id. de tabla en la estructura out. Las columnas creadas dentro de la tabla tienen un identificador de columna único o COLUMN_ID. Los id. de columnas se crean en las llamadas a [JetAddColumn](./jetaddcolumn-function.md)o en las llamadas a [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)o [JetOpenTempTable3](./jetopentemptable3-function.md) para tablas temporales. Los id. de columna también se pueden recuperar para una columna determinada por su nombre con API como [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).
