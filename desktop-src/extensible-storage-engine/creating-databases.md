---
description: Más información acerca de cómo crear bases de datos
title: Crear bases de datos
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715414"
---
# <a name="creating-databases"></a>Crear bases de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="creating-databases"></a>Crear bases de datos

La base de datos ESE consta de una o varias tablas que organizan los datos por columnas y filas. La base de datos ESE se identifica mediante el nombre y el identificador de base de datos. Una base de datos ESE es similar a un único archivo del sistema operativo Microsoft Windows; sin embargo, internamente, la base de datos se almacena como una colección de páginas. Estas páginas contienen metadatos que describen los datos de la base de datos, los propios datos y uno o varios índices que almacenan diferentes pedidos de los datos. La base de datos puede contener hasta 2 ^ 31 páginas o 16 terabytes de datos para una base de datos con páginas de 8 KB.

La aplicación crea una instancia del motor de base de datos y, a continuación, crea una base de datos y la asocia a la instancia. Hasta 6 bases de datos se pueden adjuntar simultáneamente a una instancia con [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetAttachDatabase](./jetattachdatabase-function.md). Se deben iniciar una o varias sesiones en la base de datos, ya que todas las operaciones de ESE subsiguientes se realizan en el contexto de una sesión. Se debe abrir una sesión independiente para cada subproceso con ESE.

Este procedimiento inicializará ESE y creará una base de datos.

### <a name="to-initialize-ese-and-create-a-database"></a>Para inicializar ESE y crear una base de datos

1.  [JetCreateInstance](./jetcreateinstance-function.md): crea una instancia del motor de base de datos.
    
    **Windows XP y versiones posteriores:** Esta función está disponible en Windows XP y versiones posteriores. En Windows 2000, solo se admite una instancia y esa instancia se crea implícitamente.

2.  [JetSetSystemParameter](./jetsetsystemparameter-function.md): los parámetros del sistema que afectan al diseño físico, como el JET_paramLogFilePath y el JET_paramSystemPath se deben establecer antes de inicializar la instancia con [JetInit](./jetinit-function.md). Los parámetros establecidos en esta fase se establecen para todas las bases de datos creadas en la instancia. [JetSetSystemParameter](./jetsetsystemparameter-function.md) es la única función que puede usar la instancia antes de que se inicialice con [JetInit](./jetinit-function.md).

3.  [JetInit](./jetinit-function.md): Inicializa la instancia. La instancia se debe inicializar con [JetInit](./jetinit-function.md) para poder usarse con cualquier otra función.

4.  [JetBeginSession](./jetbeginsession-function.md): crea la sesión para todas las transacciones posteriores. Todas las transacciones de base de datos tienen lugar en el contexto de la sesión ([JET_SESID](./jet-sesid.md)).

5.  [JetCreateDatabase](./jetcreatedatabase-function.md): crea la base de datos y devuelve un identificador al identificador de la base de datos ([JET_DBID](./jet-dbid.md)).
    
    Si la base de datos ya existe, el paso 5 anterior se sustituye por los dos pasos siguientes:
    
    1.  [JetAttachDatabase](./jetattachdatabase-function.md): adjunta la base de datos por nombre a la sesión.
    
    2.  [JetOpenDatabase](./jetopendatabase-function.md): devuelve el identificador de base de datos que se utiliza en las operaciones de base de datos subsiguientes.

Una base de datos se puede desasociar de una instancia de ESE mediante [JetDetachDatabase](./jetdetachdatabase-function.md) y posteriormente se adjunta a otra instancia con [JetAttachDatabase](./jetattachdatabase-function.md). Cuando la base de datos se separa, se puede copiar como un archivo único mediante las utilidades estándar de Windows. Sin embargo, cuando la base de datos se adjunta a una instancia de ESE, no se puede copiar, ya que ESE abre exclusivamente archivos de base de datos. Además, si la instancia se bloquea, el archivo de base de datos no se puede copiar por sí solo porque necesita los archivos de registro de transacciones asociados para recuperarse de ese bloqueo.
