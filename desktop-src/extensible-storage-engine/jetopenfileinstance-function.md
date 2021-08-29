---
description: 'Más información sobre: JetOpenFileInstance (Función)'
title: Función JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ce54e03c79f8147b1deb9f77bab520c6d2b121e9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480371"
---
# <a name="jetopenfileinstance-function"></a>Función JetOpenFileInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopenfileinstance-function"></a>Función JetOpenFileInstance

La **función JetOpenFileInstance** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming. Posteriormente, los datos de estos archivos se pueden leer a través del identificador devuelto [mediante JetReadFileInstance](./jetreadfileinstance-function.md). El identificador devuelto debe cerrarse [mediante JetCloseFileInstance.](./jetclosefileinstance-function.md) Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).

**Windows XP:****JetOpenFileInstance** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

Para Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

Para Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación JET_errRunningInMultiInstanceMode.

*szFileName*

Ruta de acceso relativa o absoluta a una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones administrado por la instancia de que se lee para la copia de seguridad.

*phfFile*

Puntero al búfer de salida que recibe un identificador para el archivo que se va a leer.

*pulFileSizeLow*

Puntero al búfer de salida que recibe los 32 bits menos significativos del tamaño del archivo.

*pulFileSizeHigh*

Puntero al búfer de salida que recibe los 32 bits más significativos del tamaño del archivo.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>Error en la operación porque no pudo abrir el archivo solicitado debido a una infracción de uso compartido o a privilegios insuficientes.</p> | 
| <p>JET_errFileNotFound</p> | <p>Error en la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada. Este error solo lo devolverá Windows 2000.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia.</p> | 
| <p>JET_errInvalidPath</p> | <p>Error en la operación porque no se encontró la ruta de acceso especificada.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetOpenFileInstance</strong> cuando:</p><ul><li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></li><li><p>El parámetro filename especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</p></li></ul> | 
| <p>JET_errMissingFileToBackup</p> | <p>No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla. <strong>JetOpenFileInstance</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que JetCloseFileInstance haya cerrado el archivo anterior abierto mediante <strong>JetOpenFileInstance.</strong> <a href="gg269270(v=exchg.10).md"></a> Actualmente solo se admite un identificador de archivo pendiente.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (Windows modo de compatibilidad 2000), donde solo se admite una instancia cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, se devuelve un identificador para el archivo solicitado. Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para una copia de seguridad de streaming que puede dar lugar a la creación de un archivo de revisión de base de datos en la misma ubicación que el archivo de base de datos. El archivo de revisión de base de datos tiene exactamente la misma ruta de acceso y nombre de archivo que el archivo de base de datos, pero con un . Extensión PAT. También se devolverá el tamaño del archivo.

En caso de error, el estado de los búferes de salida será indefinido. Se puede crear temporalmente un archivo de revisión de base de datos en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión. El error provocará la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se intentó realizar una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.

**Advertencia**  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFileInstance** no comprueba que la ruta de acceso de archivo solicitada está asociada al conjunto de archivos de los que se realiza una copia de seguridad para la instancia. Como resultado, es posible usar esta función para acceder a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso. Es fundamental que la aplicación restrinja las rutas de acceso que se pasan a esta función a un conjunto conocido de rutas de acceso de archivo correctas o que se pueda hacer posible la divulgación de ataques de información.

#### <a name="remarks"></a>Comentarios

Los búferes de salida de tamaño de archivo y identificador deben estar presentes. Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.

En este momento, solo se puede abrir un archivo para la copia de seguridad a la vez.

**JetOpenFileInstance** no declara el privilegio de copia de seguridad antes de abrir el archivo solicitado.

Es posible que el tamaño del archivo que se va a leer como notifica esta función no coincida con el tamaño del archivo en disco. En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos utilizado por el motor de base de datos durante una operación de restauración. Por lo tanto, la aplicación solo debe basarse en el tamaño de archivo devuelto por **JetOpenFileInstance** o en el número real de bytes de datos devueltos por [JetReadFileInstance](./jetreadfileinstance-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetOpenFileInstanceW</strong> (Unicode) y <strong>JetOpenFileInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFileInstance](./jetclosefileinstance-function.md)  
[JetGetAttachInfoInstance](./jetgetattachinfoinstance-function.md)  
[JetGetLogInfoInstance](./jetgetloginfoinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetTruncateLogInstance](./jettruncateloginstance-function.md)
