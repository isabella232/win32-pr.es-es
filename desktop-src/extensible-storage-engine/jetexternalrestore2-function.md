---
description: 'Más información acerca de: JetExternalRestore2 (función)'
title: Función JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002411"
---
# <a name="jetexternalrestore2-function"></a>Función JetExternalRestore2


_**Se aplica a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Función JetExternalRestore2

La función **JetExternalRestore2** restaura una copia de seguridad externa que se tomó con las API de copia de seguridad externas y proporciona puntos de control que se utilizan para las operaciones de registro circulares. Esto se conoce como recuperación de hardware, que es similar pero diferente a la recuperación de software que realiza la función [JetInit](./jetinit-function.md) .

**Windows XP: JetExternalRestore2** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parámetros

*szCheckpointFilePath*

La ruta de acceso del archivo de punto de comprobación que se va a usar durante la recuperación si no se especifica *szTargetInstanceCheckpointPath* o si la ruta de acceso tiene una instancia activa o en ejecución.

*szLogPath*

La ruta de acceso o el directorio de los registros de la fase final (Deshacer) de la recuperación y, posiblemente, de los registros de puesta al día. Esta ruta de acceso puede ser la misma que la *szBackupLogPath*.

*rgrstmap*

Se trata de una matriz de estructuras [JET_RSTMAP](./jet-rstmap-structure.md) . Se trata de una asignación de nombres de archivo o rutas de acceso de base de datos antiguos y nuevos. Se usa porque las bases de datos pueden tener que recuperarse en una ubicación distinta de la ubicación desde la que se realizó la copia de seguridad. En el caso de que varias bases de datos se adjunten a un único conjunto de registros, la asignación de restauración puede especificar un subconjunto de las bases de datos que se van a restaurar.

*crstfilemap*

El número de entradas en el parámetro de matriz *rgrstmap* .

*szBackupLogPath*

La ruta de acceso al directorio donde se restauran los archivos de registro. Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa. Esta ruta de acceso puede ser la misma que la *szLogPath*.

*pLogInfo*

*PLogInfo* describe varios aspectos de los registros de copia de seguridad que se van a recuperar. este parámetro permite a **JetExternalRestore2** tomar los parámetros *genLow* y *genHigh* explícitos que **JetExternalRestore2** tiene, así como el nombre de registro base, en lugar de un nombre de base de registro supuestamente "edb".

*szTargetInstanceName*

Este parámetro está en desuso y no se puede usar en la aplicación.

*szTargetInstanceLogPath*

La ruta de acceso para los registros de puesta al día si la ubicación de los registros que le gustaría poner al día se encuentran en un conjunto de registros o una instancia activos. No debe especificarse si la instancia de de destino utiliza el registro circular.

*szTargetInstanceCheckpointPath*

La ruta de acceso del punto de comprobación durante la recuperación si no hay ninguna instancia activa en ejecución en este destino. No debe especificarse si la instancia de de destino utiliza el registro circular.

*pfn*

La devolución de llamada de estado, que informa del progreso de la recuperación.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>El <em>szTargetInstanceLogPath</em> especificado no pertenece a una instancia inicializada. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Esto indica que la base de datos está dañada o un archivo no reconocido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro anterior que se especifica en <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican. Es decir, deben coincidir y estar especificados o no especificados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Se devuelve este error si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se hizo copia de seguridad con copia de seguridad externa.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>El motor de base de datos no puede ejecutar la restauración externa o la recuperación de hardware en modo de instancia única. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro por debajo de la que especifica <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente. En este momento, la base de datos se puede volver a montar en una instancia existente.

En caso de error, el motor no pudo recuperar la base de datos. La base de datos está en un estado no válido y, para volver a intentar la recuperación de hardware, se debe restaurar toda la base de datos. Normalmente, el origen de esta situación es el disco o el registro dañado, o algún otro tipo de administración incorrecta del registro, o un conjunto de registros no continuos.

#### <a name="remarks"></a>Observaciones

Vea [JetExternalRestore](./jetexternalrestore-function.md).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetExternalRestore2W</strong> (Unicode) y <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
