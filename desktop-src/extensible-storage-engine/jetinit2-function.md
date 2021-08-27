---
description: 'Más información sobre: Función JetInit2'
title: Función JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b5d2a62aa448a84d539d8d2d557d06befacfbba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988958"
---
# <a name="jetinit2-function"></a>Función JetInit2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetinit2-function"></a>Función JetInit2

La **función JetInit2 coloca** el motor de base de datos en un estado en el que puede admitir el uso de archivos de base de datos de la aplicación. El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md). La recuperación de bloqueos de base de datos se realiza automáticamente como parte del proceso de inicialización.

**Windows XP:****JetInit2** se introdujo en Windows XP.  

Esta función está obsoleta. Use [JetInit3 en](./jetinit3-function.md) su lugar.

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*pinstance*

Instancia de que se va a usar para esta llamada.

Para Windows 2000, este parámetro se omite y siempre debe ser NULL.

Para Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o puede establecerse en un búfer de salida válido que contenga NULL o JET_instanceNil que devuelva el identificador de instancia global creado como efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que tome una instancia. Si el motor funciona en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Esta opción permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, sin que todas las bases de datos estuvieran presentes, que se adjuntaron en un punto del conjunto de registros.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Realice la recuperación, pero detenga en la fase de deshacer. Esto permite que se copien y se apliquen registros de transacciones adicionales.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Si la recuperación automática se realiza correctamente, trunca los archivos de registro.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Falta la entrada del mapa de base de datos de forma predeterminada en la misma ubicación.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Omitir los registros perdidos desde el final de la secuencia de registro.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Observaciones

Una instancia de debe inicializarse con una llamada a **JetInit2** antes de que pueda ser utilizada por cualquier otro elemento que no [sea JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm,](./jetterm-function.md) incluso si esa instancia nunca se inicializó [mediante JetInit](./jetinit-function.md). Una instancia de es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos usados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

Si la recuperación se ejecuta en un conjunto de registros, para los que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, el bitReplayIgnoreMissingDB de JET_ se usa para continuar con la recuperación de las bases de datos disponibles.

Consulte la sección Comentarios de [JetInit](./jetinit-function.md) para obtener más información.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros de recursos](./resource-parameters.md)
