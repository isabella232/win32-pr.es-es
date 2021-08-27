---
description: 'Más información sobre: JetInit (Función)'
title: Función JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d074e07dec88bf0b33ec56b1391986758fbd388c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984538"
---
# <a name="jetinit-function"></a>Función JetInit


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetinit-function"></a>Función JetInit

La **función JetInit** coloca el motor de base de datos en un estado en el que puede admitir el uso de archivos de base de datos de la aplicación. El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md). La recuperación de bloqueos de base de datos se realiza automáticamente como parte del proceso de inicialización.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parámetros

*pinstance*

Instancia de que se va a usar para esta llamada.

Para Windows 2000, este parámetro se omite y siempre debe ser NULL.

Para Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o puede establecerse en un búfer de salida válido que devolverá el identificador de instancia global creado como efecto secundario de la inicialización. Este búfer de salida debe establecerse en NULL o JET_instanceNil. A continuación, este identificador de instancia se puede pasar a cualquier otra función que use una instancia de . Si el motor funciona en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por la instancia de [función JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.


#### <a name="remarks"></a>Observaciones

Una instancia de debe inicializarse con una llamada a **JetInit** antes de que pueda ser utilizada por cualquier otro elemento que no [sea JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm,](./jetterm-function.md) incluso si esa instancia nunca se inicializó **mediante JetInit**. Una instancia de es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos usados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

El número máximo de instancias que se pueden crear en cualquier momento se controla mediante JET_paramMaxInstances [,](./resource-parameters.md)que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Cuando el motor de base de datos se inicializa por primera vez, **JetInit** creará un conjunto inicial de archivos para admitir esa instancia. Estos archivos incluyen un archivo de punto de comprobación (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un conjunto de archivos de registro de transacciones reservados (denominado RES1. LOG y RES2. LOG), un archivo de registro de transacciones inicial (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) y un archivo de base de datos temporal (denominado según [JET_paramTempPath](./temporary-database-parameters.md)). Si [JET_paramRecovery](./transaction-log-parameters.md) está establecido en "Desactivado", no se crearán el archivo de punto de comprobación ni los archivos de registro. Si [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) se establece en cero, no se creará el archivo de base de datos temporal. Estos archivos representan la superficie en disco de una instancia y deben administrarse con cuidado. Si estos archivos están dañados individualmente o con respecto a otros, es posible que se pierdan los datos almacenados en las bases de datos asociadas a la instancia.

Cuando el motor de base de datos se inicializa con un conjunto existente de archivos de registro de transacciones, esos archivos se inspeccionarán para ver si la anterior ejecución de la instancia ha sufrido un bloqueo. Si se detecta un bloqueo, se realizará automáticamente la recuperación de bloqueos. Este proceso reconstruirá las bases de datos adjuntas a la instancia durante la anterior ejecución del motor y guardará los cambios de nuevo en los archivos de base de datos. El resultado serán bases de datos coherentes con las transacciones. Este proceso puede tardar bastante tiempo si el número de archivos de registro de transacciones que se reproducen en las bases de datos es grande.

Debido al hecho de que **JetInit** realiza la recuperación de bloqueos, es posible que casi cualquier error del motor de base de datos se devuelva en caso de error. En la práctica, la mayoría de los errores detectados en la implementación se divide en dos categorías: daños en los datos y administración de archivos. Los datos dañados se manifiestan con más frecuencia en los errores siguientes o similares:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Estos errores casi siempre se deben a problemas de hardware y, por tanto, no se pueden evitar. La administración errónea de archivos se manifesta con más frecuencia en los errores siguientes o similares:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Si la recuperación se ejecuta en un conjunto de registros, para los que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, se puede usar el bitReplayIgnoreMissingDB de JET_ para continuar con la recuperación de las bases de datos disponibles. La aplicación puede evitar estos errores. La aplicación debe tener cuidado de proteger el repositorio de estos archivos de la manipulación por parte de fuerzas externas, como el usuario u otras aplicaciones. Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia. Estos incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos asociados a la instancia.

La **función JetInit** se comporta de forma diferente, con respecto a los archivos de base de datos asociados a la instancia, entre Windows 2000 y versiones posteriores.

**Windows 2000:**  En Windows 2000, cualquier base de datos asociada a la instancia durante una ejecución anterior de esa instancia permanece asociada a la instancia después de que **JetInit** se complete correctamente. No es necesario llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit** para garantizar el acceso posterior a la base de datos. Si se [llama a la función JetAttachDatabase](./jetattachdatabase-function.md) después de la función **JetInit,** se devolverá JET_wrnDatabaseAttached advertencia. Esta advertencia indica que los datos adjuntos de la base de datos se conservaron y se pueden omitir.

**Windows XP:**  En Windows XP y versiones posteriores, **JetInit** desasocia automáticamente todas las bases de datos de la instancia de . Esto significa que siempre se debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después **de JetInit** en este caso.

Cualquier aplicación escrita para ejecutarse en Windows 2000 y en versiones posteriores siempre debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después **de JetInit**. Si la aplicación se ejecuta Windows 2000, debe esperar ver JET_wrnDatabaseAttached en algunos casos. Consulte [JetAttachDatabase para](./jetattachdatabase-function.md) obtener más información.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
