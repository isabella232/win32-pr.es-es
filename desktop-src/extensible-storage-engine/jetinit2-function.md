---
description: 'Más información acerca de: JetInit2 (función)'
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
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104004002"
---
# <a name="jetinit2-function"></a>Función JetInit2


_**Se aplica a:** Windows | Windows Server_

## <a name="jetinit2-function"></a>Función JetInit2

La función **JetInit2** coloca el motor de base de datos en un estado en el que pueda admitir el uso de aplicaciones de archivos de base de datos. El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md). La recuperación tras bloqueo de la base de datos se realiza automáticamente como parte del proceso de inicialización.

**Windows XP:**  **JetInit2** se presentó en Windows XP.

Esta función está obsoleta. Use [JetInit3](./jetinit3-function.md) en su lugar.

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*pinstance*

Instancia de que se va a usar para esta llamada.

En Windows 2000, este parámetro se omite y siempre debe ser NULL.

En Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o se puede establecer en un búfer de salida válido que contenga NULL o JET_instanceNil que devuelva el identificador de instancia global creado como un efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que toma una instancia. Si el motor está funcionando en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por el [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

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
<td><p>Reservado para uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Esta opción permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, sin que estén presentes todas las bases de datos, que se adjuntaron en un punto del conjunto de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Realiza la recuperación, pero se detiene en la fase de deshacer. Esto permite que se copien y se apliquen registros de transacciones adicionales.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>En la recuperación de software correcta, trunque los archivos de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Falta la entrada de asignación de base de datos predeterminada en la misma ubicación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Omitir los registros perdidos desde el final de la secuencia de registro.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> se introduce en Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).


#### <a name="remarks"></a>Observaciones

Una instancia de se debe inicializar con una llamada a **JetInit2** para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con [JetInit](./jetinit-function.md). Una instancia es la unidad de capacidad de recuperación del motor de base de datos. Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos. Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.

Si la recuperación se está ejecutando en un conjunto de registros, para el que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, el JET_ bitReplayIgnoreMissingDB se usa para continuar la recuperación de las bases de datos disponibles.

Vea la sección Comentarios en [JetInit](./jetinit-function.md) para obtener más información.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros de recursos](./resource-parameters.md)
