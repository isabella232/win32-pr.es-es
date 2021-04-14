---
description: 'Más información acerca de: JetInit3 (función)'
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
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361683"
---
# <a name="jetinit3-function"></a>Función JetInit3


_**Se aplica a:** Windows | Windows Server_

## <a name="jetinit3-function"></a>Función JetInit3

La función **JetInit3** coloca el motor de base de datos en un estado en el que puede admitir el uso de aplicaciones de archivos de base de datos. El motor ya debe estar configurado correctamente para la inicialización, lo que se realiza mediante la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) . Tenga en cuenta que la recuperación tras bloqueo de la base de datos se produce automáticamente como parte del proceso de inicialización.

**Windows Vista:**  **JetInit3** se presentó en Windows Vista.

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

La instancia de que se usa para una llamada determinada. El uso de este parámetro depende del modo de funcionamiento del motor. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000), en el que solo se admite una instancia, puede establecer este parámetro en **null** o en un búfer de salida válido que contenga **null** o JET_instanceNil, que devuelve el identificador de instancia global creado como efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que toma una instancia. Si el motor está funcionando en modo de varias instancias, debe establecer este parámetro en un búfer de entrada válido que contenga el identificador de instancia devuelto por la función [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*prstInfo*

Parámetros de recuperación adicionales que se usan para reasignar las bases de datos durante la recuperación, para establecer la posición en la que se detendrá la recuperación o para determinar el estado de recuperación actual.

*grbit*

Grupo de bits que especifica cero o más de las opciones enumeradas y definidas en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Este valor está reservado para uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Este valor está reservado para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Este valor permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, incluso en ausencia de las bases de datos que se adjuntaron al archivo de registro establecido en algún momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Este valor permite al usuario realizar la recuperación, pero solo hasta (y sin incluir) la fase de deshacer. Con este valor, se pueden copiar y aplicar registros de transacciones adicionales.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Este valor hace que se trunquen los archivos de registro durante una recuperación de software correcta.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Este valor hace que la entrada de asignación de base de datos que falta se encuentre en la misma ubicación de forma predeterminada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Este valor hace que se omitan los registros perdidos desde el final de la secuencia de registro durante una recuperación.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> se introduce en Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).


#### <a name="remarks"></a>Observaciones

Una instancia de se debe inicializar con una llamada a la función **JetInit3** antes de que pueda ser utilizada por cualquier cosa que no sea la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó mediante la función [JetInit](./jetinit-function.md) . Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones. Tenga en cuenta que no se debe llamar a [JetTerm](./jetterm-function.md) si se produce un error en la función **JetInit3** . Sin embargo, todavía se debe llamar a [JetTerm](./jetterm-function.md) para todas las instancias creadas por **JetCreateInstance2** si nunca se llamó a **JetInit3** o si **JetInit3** se realiza correctamente.

Si la recuperación se está ejecutando en un conjunto de registros para el que no están presentes todas las bases de datos relacionadas (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, se usa el error de JET_bitReplayIgnoreMissingDB para continuar la recuperación de las bases de datos disponibles.

Dado que la recuperación tras bloqueo no suele producirse en el mismo equipo (y con la misma configuración) que en el momento del bloqueo, una base de datos no suele cambiar la ubicación. En algunos escenarios, como el traslado de archivos a una máquina diferente o la restauración de la copia de seguridad de instantáneas en ubicaciones diferentes, esto ya no es así. La función **JetInit3** permite especificar una asignación (mediante las estructuras [JET_RSTINFO](./jet-rstinfo-structure.md) y [JET_RSTMAP](./jet-rstmap-structure.md) ) entre la antigua ubicación de la base de datos y su nueva ubicación. De hecho, solo necesita la nueva ubicación, siempre y cuando los archivos de base de datos estén presentes en esa ubicación. En cuanto Conozca las ubicaciones de las bases de datos restauradas, la firma de la base de datos se utilizará para identificar la base de datos a través del proceso de restauración. Solo necesitará la ubicación de la base de datos original si necesita volver a crear una base de datos, en cuyo caso se conoce la firma.

Además, si necesita detener una recuperación después de una operación de deshacer, puede especificar una posición de registro determinada en la que se detendrá la recuperación. Tenga en cuenta que esto incluye la capacidad de detenerse al final de una generación de registro determinada si la posición especificada forma parte de la generación pero supera el final del registro real.

Para obtener más información, vea la sección "Comentarios" en el tema [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Remoto</p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p>Encabezado</p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Utiliza ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>Archivo DLL</p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Se implementa como <strong>JetInit3W</strong> (Unicode) y <strong>JetInit3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
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
