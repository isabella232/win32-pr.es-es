---
description: 'Más información acerca de: identificadores de ESE'
title: Identificadores de ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278538"
---
# <a name="ese-handles"></a>Identificadores de ESE


_**Se aplica a:** Windows | Windows Server_

## <a name="ese-handles"></a>Identificadores de ESE

Los identificadores de ESE se utilizan para crear sesiones y obtener acceso a bases de datos. Se mantienen en una jerarquía, lo que significa que la salida de un nivel se usa para tener acceso a los recursos en el siguiente nivel.

En el diagrama siguiente se muestra la jerarquía de identificadores y las funciones correspondientes que crean los identificadores. También se indica junto con las funciones son los identificadores que se usan en la llamada para crear el nuevo identificador.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Como se muestra en el diagrama, la instancia es el identificador raíz y el nivel en el que se recupera la base de datos en caso de que se produzca una terminación de proceso inesperada o un cierre del sistema. El identificador de instancia, JET_INSTANCE, se crea mediante [JetCreateInstance](./jetcreateinstance-function.md) y [JetCreateInstance2](./jetcreateinstance2-function.md). El nivel siguiente, el nivel de sesión, es el contexto de transacción del motor de base de datos y el nivel en el que se realizan todas las operaciones de base de datos. El identificador de sesión, JET_SESID, se crea en el contexto de la instancia de en la llamada a [JetBeginSession](./jetbeginsession-function.md). El identificador de sesión se utiliza en todas las llamadas subsiguientes para tener acceso a las tablas y bases de datos. Si hay más de un subproceso utilizando la instancia a la vez, cada subproceso debe utilizar su propio identificador de sesión. El identificador de la base de datos se crea mediante el identificador de sesión y se utiliza principalmente para administrar el esquema de la base de datos, pero también se puede usar para administrar tablas dentro de la base de datos. Los identificadores de base de datos solo se pueden usar en la sesión en la que se crean. El identificador de la base de datos se crea en la llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md). Las tablas se asocian con el identificador de base de datos en el que se crean.

El tipo de datos JET_TABLEID contiene un identificador para un cursor de base de datos. Se usa para examinar registros, buscar registros o crear registros de actualización y eliminación. El identificador de la tabla se crea en la llamada a [JetOpenTable](./jetopentable-function.md)o [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)y [JetOpenTempTable3](./jetopentemptable3-function.md) también crean los ID. de tabla para las tablas temporales, y [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) y [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) devuelven los identificadores de tabla de la estructura out. Cada una de las columnas creadas en la tabla tiene un identificador de columna único o un COLUMN_ID. Los identificadores de las columnas se crean en las llamadas a [JetAddColumn](./jetaddcolumn-function.md)o en las llamadas a [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)o [JetOpenTempTable3](./jetopentemptable3-function.md) para las tablas temporales. También se pueden recuperar los identificadores de columna para una columna determinada por nombre con las API como [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).
