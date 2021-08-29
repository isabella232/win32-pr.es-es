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
ms.openlocfilehash: 91eb8ffe90d44435b6318c2456903ce978599c66
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984488"
---
# <a name="jetopenfile-function"></a>Función JetOpenFile


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopenfile-function"></a>Función JetOpenFile

La **función JetOpenFile** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming. Posteriormente, los datos de estos archivos se pueden leer a través del identificador devuelto [mediante JetReadFile](./jetreadfile-function.md). El identificador devuelto debe cerrarse [mediante JetCloseFile.](./jetclosefile-function.md) Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

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


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>Error en la operación porque no pudo abrir el archivo solicitado debido a una infracción de uso compartido o a privilegios insuficientes.</p> | 
| <p>JET_errFileNotFound</p> | <p>Error en la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada. Este error solo lo devolverá Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetOpenFile</strong> cuando:</p><ul><li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></li><li><p>El parámetro filename especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Error en la operación porque no se encontró la ruta de acceso especificada.</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla. <strong>JetOpenFile</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que <strong>JetCloseFile</strong> haya cerrado el archivo anterior abierto mediante <a href="gg294127(v=exchg.10).md">JetOpenFile.</a> Actualmente solo se admite un identificador de archivo pendiente.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando, de hecho, ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión. JET_errRestoreInProgress No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, se devolverá un identificador al archivo solicitado. Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para la copia de seguridad de streaming, lo que puede dar lugar a la creación de un archivo de revisión de base de datos en la misma ubicación que el archivo de base de datos. El archivo de revisión de base de datos tiene exactamente la misma ruta de acceso y nombre de archivo que el archivo de base de datos, pero tiene un . Extensión PAT. También se devolverá el tamaño del archivo.

En caso de error, el estado de los búferes de salida será indefinido. Se puede crear temporalmente un archivo de revisión de base de datos en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión. El error provocará la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se intentó realizar una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.

**Advertencia**  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFile** no comprueba que la ruta de acceso del archivo solicitado está asociada al conjunto de archivos de los que se debe realizar una copia de seguridad para la instancia. Como resultado, es posible usar esta función para acceder a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso. Es fundamental que la aplicación restrinja las rutas de acceso que se pasan a esta función a un conjunto conocido de rutas de acceso de archivo correctas o que se pueda hacer posible la divulgación de ataques de información.

#### <a name="remarks"></a>Observaciones

Los búferes de salida de tamaño de archivo y identificador deben estar presentes. Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.

En este momento, solo se puede abrir un archivo para la copia de seguridad en cualquier momento.

**JetOpenFile** no declara el privilegio de copia de seguridad antes de abrir el archivo solicitado.

Es posible que el tamaño del archivo que se va a leer como notifica esta función no coincida con el tamaño del archivo en disco. En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos utilizado por el motor de base de datos durante una operación de restauración. Por lo tanto, la aplicación solo debe basarse en el tamaño de archivo devuelto por **JetOpenFile** o en el número real de bytes de datos devueltos [por JetReadFile](./jetreadfile-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetOpenFileW</strong> (Unicode) y <strong>JetOpenFileA</strong> (ANSI).</p> | 



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
