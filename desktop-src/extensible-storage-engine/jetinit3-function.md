---
description: 'Más información sobre: JetInit3 (Función)'
title: Función JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a0c73343550768a9ccd061c702fae89d562d095
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477911"
---
# <a name="jetinit3-function"></a>Función JetInit3


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetinit3-function"></a>Función JetInit3

La **función JetInit3** coloca el motor de base de datos en un estado en el que puede admitir el uso de aplicaciones de archivos de base de datos. El motor ya debe estar configurado correctamente para la inicialización, lo que se logra mediante la [función JetSetSystemParameter.](./jetsetsystemparameter-function.md) Tenga en cuenta que la recuperación de bloqueos de la base de datos se produce automáticamente como parte del proceso de inicialización.

**Windows Vista:****JetInit3** se introdujo en Windows Vista.  

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Instancia de que se usa para una llamada determinada. El uso de este parámetro depende del modo de funcionamiento del motor. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000), en el que solo se admite una instancia, puede establecer este parámetro en **NULL** o en un búfer de salida válido que contenga **NULL** o JET_instanceNil, que devuelve el identificador de instancia global creado como efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que tome una instancia. Si el motor funciona en modo de varias instancias, debe establecer este parámetro en un búfer de entrada válido que contenga el identificador de instancia devuelto por la función [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*prstInfo*

Parámetros de recuperación adicionales usados para volver a crear bases de datos durante la recuperación, para establecer la posición donde se detendrá la recuperación o para determinar el estado de recuperación actual.

*grbit*

Grupo de bits que especifica cero o más de las opciones enumeradas y definidas en la tabla siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Este valor está reservado para uso futuro.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Este valor está reservado para uso futuro.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Este valor permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, incluso en ausencia de las bases de datos que se asociaron al conjunto de archivos de registro en algún momento.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Este valor permite al usuario realizar la recuperación, pero solo hasta (y sin incluir) la fase de deshacer. Con este valor, se pueden copiar y aplicar registros de transacciones adicionales.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Este valor hace que los archivos de registro se truncan durante una recuperación de software correcta.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Este valor hace que una entrada de mapa de base de datos que falta se de forma predeterminada en la misma ubicación.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Este valor hace que los registros perdidos desde el final de la secuencia de registro se ignoren durante una recuperación.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Comentarios

Una instancia debe inicializarse con una llamada a la función **JetInit3** antes de que pueda ser utilizada por cualquier otro elemento que no sea la [función JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Una instancia se destruye mediante una llamada a la función [JetTerm,](./jetterm-function.md) incluso si esa instancia nunca se inicializó mediante la [función JetInit.](./jetinit-function.md) Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos usados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones. Tenga en cuenta que no se debe llamar a [JetTerm](./jetterm-function.md) si se produce un error **en la función JetInit3.** Sin embargo, todavía se debe llamar a [JetTerm](./jetterm-function.md) para todas las instancias creadas por **JetCreateInstance2** si nunca se llamó a **JetInit3** o si **JetInit3** se realiza correctamente.

Si la recuperación se ejecuta en un conjunto de registros para los que no todas las bases de datos relacionadas están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, el error JET_bitReplayIgnoreMissingDB se usa para continuar con la recuperación de las bases de datos disponibles.

Dado que la recuperación de bloqueos no suele producirse en la misma máquina (y con la misma configuración) que en el momento del bloqueo, una base de datos normalmente no cambia de ubicación. En determinados escenarios, como mover archivos a un equipo diferente o restaurar la copia de seguridad de instantáneas en ubicaciones diferentes, esto ya no es así. La **función JetInit3** permite especificar una asignación (mediante las estructuras [JET_RSTINFO](./jet-rstinfo-structure.md) y [JET_RSTMAP)](./jet-rstmap-structure.md) entre la ubicación de base de datos anterior y su nueva ubicación. De hecho, solo necesita la nueva ubicación siempre que los archivos de base de datos estén presentes en esa ubicación. En cuanto sepa las ubicaciones de las bases de datos restauradas, la firma de la base de datos se usará para identificar la base de datos a través del proceso de restauración. Solo necesitará la ubicación original de la base de datos si necesita volver a crear una base de datos, en cuyo caso se conoce la firma.

Además, si necesita detener una recuperación después de una operación deshacer, puede especificar una posición de registro determinada en la que se detendrá la recuperación. Tenga en cuenta que esto incluye la capacidad de detenerse al final de una generación de registros determinada si la posición especificada forma parte de la generación pero más allá del final del registro real.

Para obtener más información, vea la sección "Comentarios" del [tema JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p>Remoto</p> | <p>Requiere Windows Vista.</p> | | <p>Servidor</p> | <p>Requiere Windows Server 2008.</p> | | <p>Encabezado</p> | <p>Declarado en Esent.h.</p> | | <p>Biblioteca</p> | <p>Usa ESENT.lib.</p> | | <p>Archivo DLL</p> | <p>Requiere ESENT.dll.</p> | | <p>Unicode</p> | <p>Se implementa <strong>como JetInit3W</strong> (Unicode) y <strong>JetInit3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros de recursos](./resource-parameters.md)
