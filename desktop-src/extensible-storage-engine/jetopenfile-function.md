---
description: 'Más información sobre: JetOpenFile (Función)'
title: Función JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b83f48f024ba79eaa55ad4ae333e8f093cd307e5508e0bb8338ce9bbc4a1bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615065"
---
# <a name="jetopenfile-function"></a>Función JetOpenFile


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopenfile-function"></a>Función JetOpenFile

La **función JetOpenFile** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming. Los datos de estos archivos se pueden leer posteriormente a través del identificador devuelto [mediante JetReadFile](./jetreadfile-function.md). El identificador devuelto debe cerrarse [mediante JetCloseFile](./jetclosefile-function.md). Debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parámetros

*szFileName*

Ruta de acceso relativa o absoluta a una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones administrado por la instancia de que se leerá para la copia de seguridad.

*phfFile*

Búfer de salida que recibe un identificador para el archivo que se va a leer.

*pulFileSizeLow*

Búfer de salida que recibe los 32 bits menos significativos del tamaño del archivo.

*pulFileSizeHigh*

Búfer de salida que recibe los 32 bits más significativos del tamaño del archivo.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Error en la operación porque una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>anuló la copia de seguridad externa actual. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Error en la operación porque no se pudo abrir el archivo solicitado debido a una infracción de uso compartido o privilegios insuficientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Se ha producido un error en la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada. Este error solo lo devolverá Windows 2000.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Error en la operación de copia de seguridad porque se llamó fuera de secuencia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetOpenFile</strong> cuando:</p>
<ul>
<li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></li>
<li><p>El parámetro filename especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Error en la operación porque no se encontró la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar suficiente memoria para completarla. <strong>JetOpenFile</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que <strong>JetCloseFile</strong> haya cerrado el archivo anterior abierto <a href="gg294127(v=exchg.10).md">mediante JetOpenFile.</a> Actualmente solo se admite un identificador de archivo pendiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando, de hecho, ya existen varias instancias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión. JET_errRestoreInProgress No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá un identificador al archivo solicitado. Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para la copia de seguridad de streaming, lo que puede dar lugar a la creación de un archivo de revisión de base de datos en la misma ubicación que el archivo de base de datos. El archivo de revisión de base de datos tiene exactamente la misma ruta de acceso y nombre de archivo que el archivo de base de datos, pero tiene un . Extensión PAT. También se devolverá el tamaño del archivo.

En caso de error, el estado de los búferes de salida será indefinido. Se puede crear temporalmente un archivo de revisión de base de datos en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión. El error dará lugar a la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se intentó realizar una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.

**Advertencia**  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFile** no comprueba que la ruta de acceso de archivo solicitada está asociada al conjunto de archivos de los que se debe realizar una copia de seguridad para la instancia. Como resultado, es posible usar esta función para tener acceso a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso. Es imperativo que la aplicación restrinja las rutas de acceso pasadas a esta función a un conjunto conocido de rutas de acceso de archivo correctas o que se pueda hacer posible la divulgación de ataques de información.

#### <a name="remarks"></a>Comentarios

Los búferes de salida de tamaño de archivo y identificador deben estar presentes. Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.

En este momento, solo se puede abrir un archivo para la copia de seguridad en cualquier momento.

**JetOpenFile** no declara el privilegio de copia de seguridad antes de abrir el archivo solicitado.

Es posible que el tamaño del archivo que se va a leer según lo notificado por esta función no coincida con el tamaño del archivo en disco. En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos que usa el motor de base de datos durante una operación de restauración. Por lo tanto, la aplicación solo debe basarse en el tamaño de archivo devuelto por **JetOpenFile** o en el número real de bytes de datos devueltos [por JetReadFile](./jetreadfile-function.md).

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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
<td><p>Se implementa como <strong>JetOpenFileW</strong> (Unicode) y <strong>JetOpenFileA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
