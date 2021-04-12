---
description: 'Más información acerca de: JetInit (función)'
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
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362842"
---
# <a name="jetinit-function"></a>Función JetInit


_**Se aplica a:** Windows | Windows Server_

## <a name="jetinit-function"></a>Función JetInit

La función **JetInit** coloca el motor de base de datos en un estado en el que pueda admitir el uso de aplicaciones de archivos de base de datos. El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md). La recuperación tras bloqueo de la base de datos se realiza automáticamente como parte del proceso de inicialización.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parámetros

*pinstance*

Instancia de que se va a usar para esta llamada.

En Windows 2000, este parámetro se omite y siempre debe ser NULL.

En Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o se puede establecer en un búfer de salida válido que devolverá el identificador de instancia global creado como un efecto secundario de la inicialización. Este búfer de salida debe establecerse en NULL o en JET_instanceNil. Este identificador de instancia se puede pasar a cualquier otra función que use una instancia de. Si el motor está funcionando en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por la instancia de la función [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.


#### <a name="remarks"></a>Observaciones

Una instancia de se debe inicializar con una llamada a **JetInit** para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con **JetInit**. Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

El número máximo de instancias que se pueden crear en cualquier momento se controla mediante [JET_paramMaxInstances](./resource-parameters.md), que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Cuando el motor de base de datos se inicializa por primera vez, **JetInit** creará un conjunto inicial de archivos para admitir esa instancia. Estos archivos incluyen un archivo de punto de comprobación (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un conjunto de archivos de registro de transacciones reservados (denominado RES1. LOG y RES2. LOG), un archivo de registro de transacciones inicial (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) y un archivo de base de datos temporal (denominado según [JET_paramTempPath](./temporary-database-parameters.md)). Si [JET_paramRecovery](./transaction-log-parameters.md) se establece en "OFF", no se crearán los archivos de registro y de archivo de punto de comprobación. Si [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) se establece en cero, no se creará el archivo de base de datos temporal. Estos archivos representan el espacio en disco de una instancia y deben administrarse con cuidado. Si estos archivos están dañados individualmente o con respecto a otro, se pueden perder los datos almacenados en las bases de datos asociadas a la instancia.

Cuando el motor de base de datos se inicializa con un conjunto existente de archivos de registro de transacciones, se inspeccionarán esos archivos para ver si la anterior encarnación de la instancia sufrió un bloqueo. Si se detecta un bloqueo, se realizará automáticamente la recuperación de bloqueos. Este proceso reconstruirá las bases de datos adjuntas a la instancia durante la versión anterior del motor y guardará los cambios de nuevo en los archivos de base de datos. El resultado serán las bases de datos que son coherentes con las transacciones. Es posible que este proceso tarde bastante tiempo si el número de archivos de registro de transacciones que se van a reproducir en las bases de datos es grande.

Debido al hecho de que **JetInit** realiza la recuperación de bloqueos, es posible que se devuelva casi cualquier error del motor de base de datos en caso de error. En la práctica, la mayoría de los errores que se han detectado en la implementación de se dividen en dos categorías: daños en los datos y administración de errores de archivos. Los datos dañados se manifestarán a menudo en los siguientes errores o similares:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Estos errores casi siempre están causados por problemas de hardware y, por tanto, no se pueden evitar. La administración de errores de archivos se manifestará en la mayoría de los casos siguientes o similares:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Si la recuperación se está ejecutando en un conjunto de registros, para el que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, se puede usar el JET_ bitReplayIgnoreMissingDB para continuar la recuperación de las bases de datos disponibles. Estos errores son impidebles por la aplicación. La aplicación debe tener cuidado de proteger el repositorio de estos archivos contra la manipulación de las fuerzas externas, como el usuario u otras aplicaciones. Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia. Entre ellos se incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y cualquier archivo de base de datos asociado a la instancia.

La función **JetInit** se comporta de forma diferente, con respecto a los archivos de base de datos adjuntos a la instancia, entre Windows 2000 y versiones posteriores.

**Windows 2000:**  En Windows 2000, cualquier base de datos asociada a la instancia durante una encarnación anterior de esa instancia permanece adjunta a la instancia después de que **JetInit** se complete correctamente. No es necesario llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit** para garantizar el acceso posterior a la base de datos. Si se llama a la función [JetAttachDatabase](./jetattachdatabase-function.md) después de la función **JetInit** , se devolverá la JET_wrnDatabaseAttached ADVERTENCIA. Esta advertencia indica que los datos adjuntos de base de datos se conservaron y se pueden omitir.

**Windows XP:**  En Windows XP y versiones posteriores, todas las bases de datos se desasocian automáticamente de la instancia de **JetInit**. Esto significa que siempre se debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit** en este caso.

Cualquier aplicación escrita para ejecutarse en Windows 2000 y en versiones posteriores siempre debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit**. Si la aplicación se ejecuta en Windows 2000, debe esperar ver JET_wrnDatabaseAttached en algunos casos. Vea [JetAttachDatabase](./jetattachdatabase-function.md) para obtener más información.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
