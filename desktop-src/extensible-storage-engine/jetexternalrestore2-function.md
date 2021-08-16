---
description: 'Más información sobre: JetExternalRestore2 (Función)'
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
ms.openlocfilehash: 6d2cbd4a13555d754cdbc1f9c02011b5891d6d6fcfae3fea822ddf6ad9953b78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719195"
---
# <a name="jetexternalrestore2-function"></a>Función JetExternalRestore2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetexternalrestore2-function"></a>Función JetExternalRestore2

La **función JetExternalRestore2** restaura una copia de seguridad externa realizada con las API de copia de seguridad externas y proporciona puntos de control que se usarán para las operaciones de registro circulares. Esto se conoce como recuperación dura, que es similar, pero diferente de la recuperación flexible, tal como se realiza con la [función JetInit.](./jetinit-function.md)

**Windows XP: JetExternalRestore2** se introdujo en Windows XP.

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

Ruta de acceso del archivo de punto de comprobación que se usará durante la recuperación si no se especifica *szTargetInstanceCheckpointPath* o si esa ruta de acceso tiene una instancia activa o en ejecución.

*szLogPath*

Ruta de acceso o directorio para los registros de la fase final (deshacer) de la recuperación y posiblemente para los registros de reversión. Esta ruta de acceso puede ser la misma que *la de szBackupLogPath.*

*rgrstmap*

Se trata de una matriz de [JET_RSTMAP](./jet-rstmap-structure.md) estructuras. Se trata de un mapa de rutas de acceso de base de datos antiguas y nuevas o nombres de archivo. Esto se usa porque es posible que las bases de datos deban recuperarse en una ubicación que no sea la ubicación desde la que se ha hecho una copia de seguridad. En el caso de que varias bases de datos estén asociadas a un único conjunto de registro, la asignación de restauración puede especificar un subconjunto de las bases de datos que se van a restaurar.

*crstfilemap*

Número de entradas del parámetro *de matriz rgrstmap.*

*szBackupLogPath*

Ruta de acceso al directorio donde se restauran los archivos de registro. Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa. Esta ruta de acceso puede ser la misma que *la de szLogPath.*

*pLogInfo*

*pLogInfo* describe varios aspectos de los registros de copia de seguridad para la recuperación. Este parámetro permite a **JetExternalRestore2** tomar los parámetros *genLow* y *genHigh* explícitos que **tiene JetExternalRestore2,** así como el nombre del registro base, en lugar de un nombre base de registro supuesto de "edb".

*szTargetInstanceName*

Este parámetro está en desuso y no se puede usar en la aplicación.

*szTargetInstanceLogPath*

Ruta de acceso de los registros de reversión si la ubicación de los registros que desea poner al día se encuentra en un conjunto de registro activo o una instancia. No se debe especificar si la instancia de destino usa el registro circular.

*szTargetInstanceCheckpointPath*

Ruta de acceso del punto de control durante la recuperación si no hay ninguna instancia activa en ejecución en este destino. No se debe especificar si la instancia de destino usa el registro circular.

*pfn*

Devolución de llamada de estado, que informa del progreso de la recuperación.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>Esto indica que la base de datos está dañada o un archivo desconocido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registros anterior a la especificada en <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Se ha producido un error en la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir <a href="gg294088(v=exchg.10).md">para JetExternalRestore,</a>y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican ambos. Es decir, deben coincidir y especificarse o ambos sin especificar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Error en la operación porque no se encontró la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Este error se devuelve si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se ha hecho una copia de seguridad externa.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>El motor de base de datos no puede ejecutar restauración externa ni recuperación en modo de instancia única. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registros inferior a la especificada por <em>genLow</em> o <em>pLogInfo.ulGenLow</em>.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente. En este momento, la base de datos se puede volver a montar en una instancia existente.

En caso de error, el motor no pudo recuperar la base de datos. La base de datos se encuentra en un estado no válido y, para reintentar la recuperación, toda la base de datos debe restaurarse de nuevo. Normalmente, el origen de esta situación es daños en el disco o el registro, o algún otro tipo de administración de registros o un conjunto de registros no continuo.

#### <a name="remarks"></a>Comentarios

Consulte [JetExternalRestore.](./jetexternalrestore-function.md)

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa <strong>como JetExternalRestore2W</strong> (Unicode) y <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
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
