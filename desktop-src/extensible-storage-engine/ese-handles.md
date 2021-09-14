---
description: 'Más información sobre: Identificadores de ESE'
title: Identificadores de ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070309"
---
# <a name="ese-handles"></a>Identificadores de ESE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="ese-handles"></a>Identificadores de ESE

Los identificadores ese se usan para crear sesiones y acceder a bases de datos. Se mantienen en una jerarquía, lo que significa que la salida de un nivel se usa para acceder a los recursos en el siguiente nivel.

El diagrama aquí muestra la jerarquía de identificadores y las funciones correspondientes que crean los identificadores. También se indican junto con las funciones los identificadores que se usan en la llamada para crear el nuevo identificador.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Como se muestra en el diagrama, la instancia es el identificador raíz y el nivel en el que se recupera la base de datos en caso de una finalización inesperada del proceso o cierre del sistema. El identificador de instancia, JET_INSTANCE, lo crean [JetCreateInstance](./jetcreateinstance-function.md) y [JetCreateInstance2.](./jetcreateinstance2-function.md) El siguiente nivel, el nivel de sesión, es el contexto de transacción del motor de base de datos y el nivel bajo el que se realizan todas las operaciones de base de datos. El identificador de sesión, JET_SESID, se crea en el contexto de la instancia de en la llamada a [JetBeginSession](./jetbeginsession-function.md). El identificador de sesión se usa en todas las llamadas posteriores para acceder a tablas y bases de datos. Si más de un subproceso está utilizando la instancia a la vez, cada subproceso debe usar su propio identificador de sesión. El identificador de base de datos se crea mediante el identificador de sesión y se usa principalmente para administrar el esquema de la base de datos, pero también se puede usar para administrar tablas dentro de la base de datos. Los identificadores de base de datos solo se pueden usar en la sesión en la que se crean. El identificador de la base de datos se crea en la llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md). Las tablas están asociadas al identificador de base de datos con el que se crean.

El JET_TABLEID de datos contiene un identificador para un cursor de base de datos. Se usa para examinar registros, buscar registros o crear registros de actualización y eliminación. El identificador de tabla se crea en la llamada a [JetOpenTable](./jetopentable-function.md)o [JetCreateTable.](./jetcreatetable-function.md) [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)y [JetOpenTempTable3](./jetopentemptable3-function.md) también crean los id. de tabla para las tablas temporales, y [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) y [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) devuelven los id. de tabla en la estructura out. Las columnas creadas dentro de la tabla tienen un identificador de columna único o COLUMN_ID. Los id. de columnas se crean en las llamadas a [JetAddColumn](./jetaddcolumn-function.md)o en llamadas a [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)o [JetOpenTempTable3](./jetopentemptable3-function.md) para tablas temporales. Los id. de columna también se pueden recuperar para una columna determinada por nombre con API como [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)
