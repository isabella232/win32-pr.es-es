---
description: 'Más información sobre: JetReadFileInstance (Función)'
title: Función JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c278426018d4e193046b10fd5986510c8d9b7e87
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985828"
---
# <a name="jetreadfileinstance-function"></a>Función JetReadFileInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetreadfileinstance-function"></a>Función JetReadFileInstance

La **función JetReadFileInstance** recupera el contenido de un archivo abierto con la [función JetOpenFileInstance.](./jetopenfileinstance-function.md)

**Windows XP**: **JetReadFileInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia que se usará para una llamada API determinada.

Tenga en cuenta que Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

Para Windows XP y versiones posteriores, puede llamar a la variante de API que no acepta este parámetro solo cuando el motor está en modo heredado (modo de compatibilidad Windows 2000) en los casos en los que solo se admite una instancia. De lo contrario, se producirá un error en la operación y se devolverá JET_errRunningInMultiInstanceMode error.

*archivo de archivos de archivos*

Identificador del archivo que se va a leer.

*Pv*

Búfer de salida que recibirá los datos del archivo.

*Cb*

Tamaño máximo, en bytes, del búfer de salida.

*Pcb*

Cantidad real de datos de archivo recuperados.

### <a name="return-value"></a>Valor devuelto

Esta función facilita la devolución de cualquier tipo [JET_ERR](./jet-err.md) datos definidos en la API Extensible Storage Engine (ESE). Para obtener más información sobre los errores de JET, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a la <a href="gg269240(v=exchg.10).md">función JetStopService.</a> Este error solo lo devolverán los Windows XP y versiones Windows posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a la <a href="gg269240(v=exchg.10).md">función JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán los Windows XP y versiones Windows posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros especificados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>la función JetReadFileInstance</strong> cuando se produce alguna de las siguientes situaciones:</p><ul><li><p>El identificador de instancia especificado no es válido. Windows XP y versiones Windows posteriores.</p></li><li><p>El tamaño del búfer de salida no es un múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP y versiones Windows posteriores.</p></li><li><p>El tamaño del búfer de salida es menor que tres páginas de base de<a href="gg269337(v=exchg.10).md">datos (JET_paramDatabasePageSize</a>), y esta es la primera llamada a la función <strong>JetReadFileInstance</strong> para el identificador especificado. Windows XP y versiones Windows posteriores.</p></li></ul> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Error en la operación porque se detectaron daños en los datos irrecuperables al leer un archivo de registro de transacciones. Este error solo lo devolverán los Windows XP y versiones Windows posteriores.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a esta sesión aún no se ha inicializado.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Error en la operación porque se detectaron daños en los datos irrecuperables al leer una página de base de datos desde un archivo de base de datos o un archivo de revisión de base de datos.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a esta sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000) en un caso en el que solo se admite una instancia, pero ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a esta sesión.</p> | 



Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida. También se devolverá el número real de bytes recuperados. El desplazamiento de archivo en el que se producirá la siguiente lectura se avanzará en esta cantidad.

En caso de error, el estado del búfer de salida es indefinido. El error provocará la cancelación de todo el proceso de copia de seguridad para la instancia actual. En Windows XP y versiones Windows posteriores, la copia de seguridad no se cancelará si se produjo un error al leer un archivo de base de datos. Sin embargo, la copia de seguridad de ese archivo de base de datos se seguirá cancelando y el identificador correspondiente se cerrará automáticamente.

#### <a name="remarks"></a>Observaciones

Cualquier llamada a la función **JetReadFileInstance** realizada mediante un identificador que ya haya devuelto todos los datos del archivo subyacente (por ejemplo, si una llamada anterior devolvía menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente, pero devolverá cero bytes de datos.

Debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad. Es posible que tenga que experimentar para encontrar el equilibrio óptimo entre el consumo de recursos y el rendimiento para una situación determinada. En cualquier caso, el búfer de salida no debe ser inferior a 64 KB. El puntero que se pasa a **JetReadFileInstance** debe estar alineado con un límite de página de memoria (4 KB u 8 KB). Para ello, llame a la **función VirtualAlloc.**

No se admiten varias llamadas simultáneas a **JetReadFileInstance** realizadas con el mismo identificador de archivo. Esto significa que no es posible poner en cola varios búferes para la lectura simultánea en el mismo archivo para lograr un alto rendimiento secuencial. En su lugar, debe usar un único búfer grande.

Si ha configurado una instancia determinada de modo que la limpieza de páginas de la base de datos esté habilitada (consulte el parámetro JET_paramCircularLog en Parámetros del sistema [),](./extensible-storage-engine-system-parameters.md)los datos eliminados se quitarán de la base de datos como efecto secundario de una llamada [a](./transaction-log-parameters.md) **JetReadFileInstance** en el archivo de base de datos.

Es muy importante comprender cómo interactúan la copia de seguridad y los datos dañados. Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia. Se trata de una decisión de diseño consciente diseñada para protegerse frente a la pérdida de datos. Si el motor de base de datos permitió que una copia de seguridad se realizara correctamente cuando había daños en los datos, es posible que se descartara como resultado una copia de seguridad anterior sin corregir. Esto sería desafortunado porque, a continuación, sería posible corregir los daños en los datos en la instancia en directo mediante la restauración de esa copia de seguridad y la reproducción de todos los archivos de registro de transacciones en esa base de datos. En este escenario de pérdida de datos cero se supone que el registro circular no está habilitado [(consulte JET_paramCircularLog](./transaction-log-parameters.md) en [Parámetros del sistema](./extensible-storage-engine-system-parameters.md)).

También es importante comprender que los casos de daños en los datos se suelen detectar por primera vez durante la copia de seguridad de streaming. Esto se debe a que la copia de seguridad de streaming es el único proceso que examina rutinariamente cada página del archivo de base de datos. También es probable que la copia de seguridad de streaming sea el primer proceso para detectar los primeros signos de error de hardware, como se manifestó por errores intermitentes de daños en los datos, debido a la cantidad de datos recuperados por la copia de seguridad y a la velocidad a la que se recuperan los datos.

El motor de base de datos detecta daños en los datos mediante el uso de sumas de comprobación de bloques. Estas sumas de comprobación se establecen justo antes de escribir una página de base de datos y se comprueban en una página de base de datos leída. Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de los daños. Históricamente, las instancias de estos datos dañados se han originado en orígenes distintos del propio motor de base de datos.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Remoto</p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p>Server</p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p>Encabezado</p> | <p>Se declara en Esent.h.</p> | 
| <p>Biblioteca</p> | <p>Usa ESENT.lib.</p> | 
| <p>Archivo DLL</p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
