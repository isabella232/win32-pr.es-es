---
description: 'Más información sobre: JetReadFile (Función)'
title: JetReadFile (Función)
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
ms.openlocfilehash: 0c670a6ed5cdcbb4b0fa4ead2415a1e55121dfce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882684"
---
# <a name="jetreadfile-function"></a>JetReadFile (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetreadfile-function"></a>JetReadFile (Función)

La **función JetReadFile** recupera el contenido de un archivo abierto con [JetOpenFile](./jetopenfile-function.md).

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*archivo de archivos de archivos*

Identificador del archivo que se va a leer.

*Pv*

Búfer de salida que recibirá los datos del archivo.

*Cb*

Tamaño máximo en bytes del búfer de salida.

*actual*

Recibe la cantidad real de datos de archivo recuperados.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>anuló la copia de seguridad externa actual. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetReadFile</strong> cuando:</p><ul><li><p>El identificador de instancia especificado no es válido. Windows XP y versiones posteriores.</p></li><li><p>El tamaño del búfer de salida no es un múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP y versiones posteriores.</p></li><li><p>El tamaño del búfer de salida es menor que tres páginas de base de datos<a href="gg269337(v=exchg.10).md">(JET_paramDatabasePageSize</a>) y esta es la primera llamada a <strong>JetReadFile</strong> para el identificador especificado. Windows XP y versiones posteriores.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Error en la operación porque se detectaron daños en los datos no recuperables al leer una página de base de datos desde un archivo de base de datos o un archivo de revisión de base de datos.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Error en la operación porque se detectaron daños en los datos no recuperables al leer un archivo de registro de transacciones. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando, de hecho, ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida. También se devolverá el número real de bytes recuperados. El desplazamiento del archivo en el que se producirá la siguiente lectura se avanzará en esta cantidad.

En caso de error, el estado del búfer de salida no está definido. El error dará lugar a la cancelación de todo el proceso de copia de seguridad de la instancia. En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se produjo un error al leer un archivo de base de datos. Sin embargo, la copia de seguridad de ese archivo de base de datos todavía se cancelará y se cerrará automáticamente el identificador correspondiente.

#### <a name="remarks"></a>Observaciones

Cualquier llamada a **JetReadFile** mediante un identificador que ya haya devuelto todos los datos del archivo subyacente (por ejemplo, una llamada anterior devuelve menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente, pero devolverá cero bytes de datos.

Se debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad. Es posible que sea necesaria alguna experimentación para encontrar el equilibrio adecuado entre el consumo de recursos y el rendimiento de una situación determinada. El búfer de salida no debe ser inferior a 64 KB en ningún caso.

No se admiten **varias llamadas simultáneas a JetReadFile** con el mismo identificador de archivo. Esto significa que no es posible poner en cola varios búferes para leer simultáneamente en el mismo archivo para lograr un alto rendimiento secuencial. En su lugar, se debe usar un único búfer grande.

Si la instancia está configurada de forma que la limpieza de páginas de la base de datos esté habilitada (consulte JET_paramZeroDatabaseDuringBackup en Parámetros del sistema), los datos eliminados se quitarán de la base de datos como efecto secundario de una llamada a **JetReadFile** en el archivo de base de datos.

Es muy importante comprender cómo interactúan la copia de seguridad y los datos dañados. Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia. Se trata de una decisión de diseño consciente diseñada para protegerse contra la pérdida de datos. Si el motor de base de datos permitió que una copia de seguridad se realizara correctamente donde había daños en los datos, es posible que se descartara como resultado una copia de seguridad anterior sin corregir. Esto sería desafortunado, ya que sería posible corregir los daños en los datos en la instancia de live mediante la restauración de esa copia de seguridad y la reproducción de todos los archivos de registro de transacciones en esa base de datos. En este escenario de pérdida de datos cero se supone que el registro circular no está habilitado [(vea JET_paramCircularLog](./transaction-log-parameters.md) en [Parámetros del sistema](./extensible-storage-engine-system-parameters.md)).

También es importante comprender que, cuando haya daños en los datos, la copia de seguridad de streaming será el lugar más probable en el que se detectará primero. Este es el caso porque la copia de seguridad de streaming es el único proceso que examina de forma rutinaria cada página del archivo de base de datos. También es probable que la copia de seguridad de streaming sea el primer proceso para detectar los primeros signos de error de hardware, como se manifestó por errores intermitentes de daños en los datos. Esto se debe a la cantidad de datos recuperados por la copia de seguridad, así como a la velocidad a la que se recuperan.

El motor de base de datos detecta daños en los datos mediante el uso de sumas de comprobación de bloques. Estas sumas de comprobación se establecen justo antes de la escritura de una página de base de datos y se comprueban en una página de base de datos leída. Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de los daños. Históricamente, se ha descubierto que la causa predominante de estos daños procede de orígenes distintos del propio motor de base de datos.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
