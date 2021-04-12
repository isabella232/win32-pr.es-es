---
description: 'Más información acerca de: JetReadFile (función)'
title: JetReadFile función)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277857"
---
# <a name="jetreadfile-function"></a>JetReadFile función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>JetReadFile función)

La función **JetReadFile** recupera el contenido de un archivo abierto con [JetOpenFile](./jetopenfile-function.md).

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*hfFile*

Identificador del archivo que se va a leer.

*FV*

Búfer de salida que recibirá los datos del archivo.

*CB*

Tamaño máximo en bytes del búfer de salida.

*pcbActual*

Recibe la cantidad real de datos de archivo recuperados.

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
<td><p>No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetReadFile</strong> cuando:</p>
<ul>
<li><p>El identificador de instancia especificado no es válido. Windows XP y versiones posteriores.</p></li>
<li><p>El tamaño del búfer de salida no es múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP y versiones posteriores.</p></li>
<li><p>El tamaño del búfer de salida es inferior a tres páginas de base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) y se trata de la primera llamada a <strong>JetReadFile</strong> para el identificador especificado. Windows XP y versiones posteriores.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>No se pudo realizar la operación porque se detectaron daños en los datos no recuperables al leer una página de base de datos de un archivo de base de datos o un archivo de revisión de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>No se pudo realizar la operación porque se detectaron daños en los datos no recuperables al leer un archivo de registro de transacciones. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
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


Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida. También se devolverá el número real de bytes recuperados. El desplazamiento de archivo en el que se producirá la siguiente lectura será avanzado en esta cantidad.

En caso de error, el estado del búfer de salida es indefinido. El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se produce un error al leer un archivo de base de datos. Sin embargo, se cancelará la copia de seguridad de ese archivo de base de datos y el identificador correspondiente se cerrará automáticamente.

#### <a name="remarks"></a>Observaciones

Cualquier llamada a **JetReadFile** con un identificador que ya ha devuelto todos los datos del archivo subyacente (como una llamada anterior devolvió menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente pero devolverá cero bytes de datos.

Se debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad. Es posible que se requiera algún experimento para encontrar el equilibrio adecuado entre el consumo de recursos y el rendimiento de una situación determinada. En cualquier caso, el búfer de salida no debe ser inferior a 64 KB.

No se admiten varias llamadas simultáneas a **JetReadFile** con el mismo identificador de archivo. Esto significa que no es posible poner en cola varios búferes para lectura simultáneamente en el mismo archivo para lograr un alto rendimiento secuencial. En su lugar, se debe usar un único búfer grande.

Si la instancia de está configurada de modo que la limpieza de páginas de la base de datos está habilitada (vea JET_paramZeroDatabaseDuringBackup en parámetros del sistema), los datos eliminados se quitarán de la base de datos como un efecto secundario de una llamada a **JetReadFile** en el archivo de base de datos.

Es muy importante entender cómo interactúan la copia de seguridad y los datos dañados. Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia. Se trata de una decisión de diseño consciente destinada a protegerse contra la pérdida de datos. Si el motor de base de datos permitía que una copia de seguridad se realizara correctamente y hubiera daños en los datos, es posible que una copia de seguridad no dañada anterior se descartase como resultado. Esto sería desafortunado porque sería posible corregir los datos dañados en la instancia en directo restaurando esa copia de seguridad y reproduciendo todos los archivos de registro de transacciones en esa base de datos. Este escenario de cero pérdida de datos presupone que el registro circular no está habilitado (vea [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)).

También es importante comprender que, cuando se dañen los datos, la copia de seguridad de transmisión por secuencias es el lugar más probable que se detecte primero. Esto se debe a que la copia de seguridad de secuencias es el único proceso que examina rutinariamente cada una de las páginas del archivo de base de datos. También es probable que la copia de seguridad de transmisión por secuencias sea el primer proceso para detectar los primeros síntomas de errores de hardware, tal como están manifiestos de errores intermitentes de daños en los datos. Esto se debe a la cantidad de datos recuperados por la copia de seguridad, así como a la velocidad a la que se recupera.

El motor de base de datos detecta los daños en los datos mediante el uso de sumas de comprobación de bloques. Estas sumas de comprobación se establecen justo antes de la escritura de una página de base de datos y se comprueban en una lectura de página de base de datos. Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de dichos daños. Históricamente, se encontró que la causa predominante de estos daños proviene de orígenes distintos del propio motor de base de datos.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
