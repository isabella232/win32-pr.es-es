---
description: 'Más información acerca de: JetOpenFileInstance (función)'
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
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697872"
---
# <a name="jetopenfileinstance-function"></a>Función JetOpenFileInstance


_**Se aplica a:** Windows | Windows Server_

## <a name="jetopenfileinstance-function"></a>Función JetOpenFileInstance

La función **JetOpenFileInstance** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming. Posteriormente, los datos de estos archivos se pueden leer a través del controlador devuelto mediante [JetReadFileInstance](./jetreadfileinstance-function.md). El identificador devuelto debe cerrarse mediante [JetCloseFileInstance](./jetclosefileinstance-function.md). Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).

**Windows XP:**  **JetOpenFileInstance** se presentó en Windows XP.

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

*repetición*

Instancia de que se va a usar para esta llamada.

En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, se implica el uso de esta instancia global.

En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.

*szFileName*

Ruta de acceso absoluta o relativa a una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones administrado por la instancia de que se lee para la copia de seguridad.

*phfFile*

Puntero al búfer de salida que recibe un identificador del archivo que se va a leer.

*pulFileSizeLow*

Puntero al búfer de salida que recibe los 32 bits menos significativos del tamaño del archivo.

*pulFileSizeHigh*

Puntero al búfer de salida que recibe los 32 bits más significativos del tamaño del archivo.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>No se pudo realizar la operación porque no se pudo abrir el archivo solicitado debido a una infracción de uso compartido o a privilegios insuficientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada. Este error solo lo devolverá Windows 2000.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetOpenFileInstance</strong> cuando:</p>
<ul>
<li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></li>
<li><p>El parámetro FILENAME especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla. <strong>JetOpenFileInstance</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>haya cerrado el archivo anterior abierto con <strong>JetOpenFileInstance</strong> . Actualmente solo se admite un identificador de archivo pendiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devuelve un identificador al archivo solicitado. Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para una copia de seguridad de secuencias, lo que puede dar lugar a la creación de un archivo de revisión de base de datos en la misma ubicación que el archivo de base de datos El archivo de revisión de la base de datos tiene exactamente la misma ruta de acceso y el mismo nombre que el archivo de base de datos, pero con un. Extensión PAT. También se devolverá el tamaño del archivo.

En caso de error, el estado de los búferes de salida será undefined. Un archivo de revisión de base de datos puede crearse temporalmente en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión. El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, no se cancelará la copia de seguridad si se realiza un intento de hacer una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.

**ADVERTENCIA**  de  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFileInstance** no comprueba que la ruta de acceso del archivo solicitada esté asociada con el conjunto de archivos de los que se ha realizado una copia de seguridad para la instancia. Como resultado, es posible usar esta función para tener acceso a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso. Es imperativo que la aplicación restrinja las rutas de acceso que se pasan a esta función a un conjunto conocido de rutas de acceso de archivos correctas o a la revelación del ataque de información.

#### <a name="remarks"></a>Observaciones

Es necesario que los búferes de salida de identificador y tamaño de archivo estén presentes. Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.

En este momento, solo se puede abrir un archivo para copia de seguridad al mismo tiempo.

**JetOpenFileInstance** no valida el privilegio de copia de seguridad antes de abrir el archivo solicitado.

Es posible que el tamaño del archivo que se va a leer tal como lo indique esta función no coincida con el tamaño del archivo en el disco. En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos utilizado por el motor de base de datos durante una operación de restauración. Como tal, la aplicación solo debe confiar en el tamaño de archivo devuelto por **JetOpenFileInstance** o en el número real de bytes de datos devueltos por [JetReadFileInstance](./jetreadfileinstance-function.md).

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
<td><p>Se implementa como <strong>JetOpenFileInstanceW</strong> (Unicode) y <strong>JetOpenFileInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
