---
description: 'Más información sobre: Creación de bases de datos'
title: Creación de bases de datos
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 4bcd4422e40434c36b71ddc3b3adf435cd96538623b8aedc0ece0a103076f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901726"
---
# <a name="creating-databases"></a>Creación de bases de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="creating-databases"></a>Creación de bases de datos

La base de datos ese consta de una o varias tablas que organizan los datos por columnas y filas. La base de datos ese se identifica por nombre e identificador de base de datos. Una base de datos ese tiene un aspecto similar a un único archivo para el sistema Windows operativo microsoft. sin embargo, internamente la base de datos se almacena como una colección de páginas. Estas páginas contienen metadatos que describen los datos de la base de datos, los propios datos y uno o varios índices que almacenan distintos pedidos de los datos. La base de datos puede contener hasta 2^31 páginas o 16 Terabytes de datos para una base de datos con páginas de 8 KB.

La aplicación crea una instancia del motor de base de datos y, a continuación, crea una base de datos y la asocia a la instancia de . Se pueden asociar simultáneamente hasta 6 bases de datos a una instancia con [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetAttachDatabase.](./jetattachdatabase-function.md) Se deben iniciar una o varias sesiones dentro de la base de datos, ya que todas las operaciones ese posteriores se realizan en el contexto de una sesión. Se debe abrir una sesión independiente para cada subproceso mediante ESE.

Este procedimiento inicializará ese y creará una base de datos.

### <a name="to-initialize-ese-and-create-a-database"></a>Para inicializar ese y crear una base de datos

1.  [JetCreateInstance:](./jetcreateinstance-function.md)crea una instancia del motor de base de datos.
    
    **Windows XP y versiones posteriores:** Esta función está disponible en Windows XP y versiones posteriores. En Windows 2000, solo se admite una instancia y esa instancia se crea implícitamente

2.  [JetSetSystemParameter:](./jetsetsystemparameter-function.md)los parámetros del sistema que afectan al diseño físico, como JET_paramLogFilePath y JET_paramSystemPath deben establecerse antes de inicializar la instancia [con JetInit](./jetinit-function.md). Los parámetros establecidos en esta fase se establecen para todas las bases de datos creadas en la instancia de . [JetSetSystemParameter es](./jetsetsystemparameter-function.md) la única función que puede usar la instancia antes de inicializarse con [JetInit.](./jetinit-function.md)

3.  [JetInit:](./jetinit-function.md)inicializa la instancia de . La instancia se debe inicializar [con JetInit para](./jetinit-function.md) poder usarse con cualquier otra función.

4.  [JetBeginSession:](./jetbeginsession-function.md)crea la sesión para todas las transacciones posteriores. Todas las transacciones de base de datos tienen lugar en el contexto de la sesión ([JET_SESID](./jet-sesid.md)).

5.  [JetCreateDatabase:](./jetcreatedatabase-function.md)crea la base de datos y devuelve un identificador al identificador de base de datos ([JET_DBID](./jet-dbid.md)).
    
    Si la base de datos ya existe, el paso 5 anterior se reemplaza por los dos pasos siguientes:
    
    1.  [JetAttachDatabase:](./jetattachdatabase-function.md)adjunta la base de datos por su nombre a la sesión.
    
    2.  [JetOpenDatabase:](./jetopendatabase-function.md)devuelve el identificador de base de datos que se usa en las operaciones de base de datos posteriores.

Una base de datos se puede desasociar de una instancia de ESE mediante [JetDetachDatabase](./jetdetachdatabase-function.md) y, posteriormente, adjuntarse a otra instancia [con JetAttachDatabase](./jetattachdatabase-function.md). Cuando se desasocia la base de datos, se puede copiar como un único archivo mediante utilidades Windows estándar. Sin embargo, cuando la base de datos está asociada a una instancia de ESE, no se puede copiar, ya que ese abre los archivos de base de datos exclusivamente. Además, si la instancia se bloquea, el archivo de base de datos no se puede copiar por sí solo porque necesita los archivos de registro de transacciones asociados a él para recuperarse de ese bloqueo.
