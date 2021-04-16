---
description: 'Más información acerca de: JetReadFileInstance (función)'
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
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539971"
---
# <a name="jetreadfileinstance-function"></a>Función JetReadFileInstance


_**Se aplica a:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>Función JetReadFileInstance

La función **JetReadFileInstance** recupera el contenido de un archivo abierto con la función [JetOpenFileInstance](./jetopenfileinstance-function.md) .

**Windows XP**:   **JetReadFileInstance** se presentó en Windows XP.

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

*repetición*

Instancia de que se va a usar para una llamada de API determinada.

Tenga en cuenta que para Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, se implica el uso de esta instancia global.

En Windows XP y versiones posteriores, puede llamar a la variante de API que no acepta este parámetro solo cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000) en casos en los que solo se admite una instancia. De lo contrario, se producirá un error en la operación y se devolverá el error JET_errRunningInMultiInstanceMode.

*hfFile*

Identificador del archivo que se va a leer.

*FV*

Búfer de salida que recibirá los datos del archivo.

*CB*

Tamaño máximo, en bytes, del búfer de salida.

*impreso*

La cantidad real de datos de archivo recuperados.

### <a name="return-value"></a>Valor devuelto

Esta función facilita la devolución de los tipos de datos [JET_ERR](./jet-err.md) definidos en la API del motor de almacenamiento extensible (ese). Para obtener más información acerca de los errores de JET, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> . Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha detectado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros especificados contenía un valor inesperado o un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para la función <strong>JetReadFileInstance</strong> cuando se produce cualquiera de las siguientes situaciones:</p>
<ul>
<li><p>El identificador de instancia especificado no es válido. Windows XP y versiones posteriores de Windows.</p></li>
<li><p>El tamaño del búfer de salida no es múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP y versiones posteriores de Windows.</p></li>
<li><p>El tamaño del búfer de salida es inferior a tres páginas de base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), y esta es la primera llamada a la función <strong>JetReadFileInstance</strong> para el identificador especificado. Windows XP y versiones posteriores de Windows.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>No se pudo realizar la operación porque se detectaron daños en los datos irrecuperables al leer un archivo de registro de transacciones. Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a esta sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>No se pudo realizar la operación porque se detectaron daños en los datos irrecuperables al leer una página de base de datos de un archivo de base de datos o un archivo de revisión de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a esta sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) en un caso en el que solo se admite una instancia, pero ya existen varias instancias.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a esta sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida. También se devolverá el número real de bytes recuperados. El desplazamiento de archivo en el que se producirá la siguiente lectura será avanzado en esta cantidad.

En caso de error, el estado del búfer de salida es indefinido. El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia actual. En Windows XP y versiones posteriores de Windows, la copia de seguridad no se cancelará si se produce un error al leer un archivo de base de datos. Sin embargo, se cancelará la copia de seguridad de ese archivo de base de datos y el identificador correspondiente se cerrará automáticamente.

#### <a name="remarks"></a>Observaciones

Cualquier llamada a la función **JetReadFileInstance** realizada mediante un identificador que ya ha devuelto todos los datos en el archivo subyacente (por ejemplo, si una llamada anterior ha devuelto menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente, pero devolverá cero bytes de datos.

Debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad. Es posible que tenga que experimentar para encontrar el equilibrio óptimo entre el consumo de recursos y el rendimiento para una situación determinada. En cualquier caso, el búfer de salida no debe ser inferior a 64 KB. El puntero que se pasa a **JetReadFileInstance** debe estar alineado con un límite de página de memoria (4 KB u 8 KB). Para ello, puede llamar a la función **VirtualAlloc** .

No se admiten varias llamadas simultáneas a **JetReadFileInstance** realizadas con el mismo identificador de archivo. Esto significa que no es posible poner en cola varios búferes para la lectura simultánea en el mismo archivo para lograr un alto rendimiento secuencial. En su lugar, debe usar un único búfer grande.

Si ha configurado una instancia determinada de modo que la limpieza de páginas de la base de datos esté habilitada (vea el parámetro [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)), los datos eliminados se quitarán de la base de datos como efecto secundario de una llamada a **JetReadFileInstance** en el archivo de base de datos.

Es muy importante entender cómo interactúan la copia de seguridad y los datos dañados. Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia. Se trata de una decisión de diseño consciente destinada a protegerse contra la pérdida de datos. Si el motor de base de datos permitía que una copia de seguridad se realizara correctamente y hubiera daños en los datos, es posible que una copia de seguridad no dañada anterior se descartase como resultado. Esto sería desafortunado porque después sería posible corregir los datos dañados en la instancia en directo restaurando esa copia de seguridad y reproduciendo todos los archivos de registro de transacciones en esa base de datos. En este escenario de pérdida de datos cero se presupone que el registro circular no está habilitado (vea [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)).

También es importante comprender que los casos de daños en los datos normalmente se detectan primero durante la copia de seguridad de streaming. Esto se debe a que la copia de seguridad de secuencias es el único proceso que examina rutinariamente cada una de las páginas del archivo de base de datos. También es probable que la copia de seguridad de transmisión por secuencias sea el primer proceso para detectar los primeros síntomas de errores de hardware como manifiestos de errores intermitentes de daños en los datos, debido a la cantidad de datos recuperados por la copia de seguridad y a la velocidad a la que se recuperan los datos.

El motor de base de datos detecta los daños en los datos mediante el uso de sumas de comprobación de bloques. Estas sumas de comprobación se establecen justo antes de que se escriba una página de base de datos y se comprueban en una lectura de página de base de datos. Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de dichos daños. Históricamente, las instancias de estos daños en los datos se originaron a partir de orígenes distintos del propio motor de base de datos.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Remoto</p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>Encabezado</p></td>
<td><p>Se declara en esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Utiliza ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>Archivo DLL</p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
