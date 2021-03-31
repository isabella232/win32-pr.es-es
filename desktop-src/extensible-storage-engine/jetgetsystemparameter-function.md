---
description: 'Más información acerca de: JetGetSystemParameter (función)'
title: JetGetSystemParameter función)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278658"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter función)

La función **JetGetSystemParameter** Lee los numerosos valores de configuración del motor de base de datos.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de que se va a usar para esta llamada.

En Windows 2000, este parámetro se omite y siempre debe ser **null**.

En Windows XP y versiones posteriores, este parámetro está ligeramente sobrecargado. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md). En cualquier caso, todos los parámetros del sistema se leen desde esa instancia. Si el motor está funcionando en modo de varias instancias, este parámetro puede ser **null** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateInstance](./jetcreateinstance-function.md). Cuando este parámetro es **null** , se lee la configuración global del parámetro del sistema (o el valor predeterminado). Cuando este parámetro es una instancia, se lee el valor del parámetro del sistema para esa instancia.

*sesid*

Sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.

*paramid*

IDENTIFICADOR del parámetro del sistema que se va a leer.

Vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.

*plParam*

Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

*szParam*

Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

*cbMax*

Tamaño máximo en bytes del búfer de salida de la cadena.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</p>
<p>Esto puede ocurrir para <strong>JetGetSystemParameter</strong> cuando:</p>
<ul>
<li><p>El ID. de parámetro del sistema especificado no es válido o no es compatible.</p></li>
<li><p>El parámetro del sistema especificado requiere que se proporcione el búfer de salida entero y que el puntero del búfer de salida sea <strong>null</strong>.</p></li>
<li><p>El parámetro del sistema especificado requiere que se proporcione un búfer de salida de cadena y que el puntero del búfer de salida sea <strong>null</strong>.</p>
<p><strong>Windows Vista:  </strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li>
<li><p>El parámetro del sistema especificado requiere que se proporcione un búfer de salida de cadena y el tamaño del búfer de salida es demasiado pequeño para aceptar una cadena terminada en NULL.</p>
<p><strong>Windows Vista:  </strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li>
<li><p>No se puede leer el parámetro del sistema especificado porque es de solo escritura.</p></li>
<li><p>El parámetro del sistema especificado solo es global y se intentó leer un valor específico de la instancia para ese parámetro del sistema. Esto solo puede ocurrir en Windows XP y versiones posteriores.</p></li>
<li><p>El parámetro del sistema especificado solo es por instancia y se intentó leer el valor global de ese parámetro del sistema. Esto solo puede ocurrir en Windows XP y versiones posteriores.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada. Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance</p></td>
<td><p>El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado. Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p>
<p><strong>Windows Vista:  </strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el valor de parámetro del sistema completo.</p>
<p>El búfer de salida se ha rellenado con tantos valores del parámetro del sistema como quepan. Si el búfer de salida tiene al menos un carácter de longitud, la cadena en el búfer de salida se terminará en NULL.</p>
<p><strong>Nota:  </strong> Este error no se devuelve en todas las versiones. Vea la sección Comentarios para obtener más información.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>No se pudo realizar la operación porque el búfer de salida era demasiado pequeño para recibir toda la configuración del parámetro del sistema.</p>
<p><strong>Nota:  </strong> Este error no se devuelve en algunos casos para preservar la compatibilidad de aplicaciones. Vea la sección Comentarios para obtener más información.</p>
<p><strong>Windows Vista:  </strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro del sistema solicitado se establecerá en el valor de ese parámetro del sistema.

En caso de error, el estado de los búferes de salida será undefined.

#### <a name="remarks"></a>Observaciones

Hay un problema importante en esta API que está presente en todas las versiones. Si se solicita un parámetro del sistema con un valor de cadena y el búfer de salida es demasiado pequeño para recibir la configuración del parámetro del sistema completo, no se devolverá JET_wrnBufferTruncated. En su lugar, se devuelve JET_errSuccess. Si la longitud de la cadena devuelta es igual al tamaño del búfer de salida menos el terminador **nulo** , el llamador debe reaccionar como si se devolviera JET_wrnBufferTruncated. Si se especifica un búfer de salida de cadena de tamaño cero, el llamador debe reaccionar como si se devolvieran JET_errInvalidParameter.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetSystemParameterW</strong> (Unicode) y <strong>JetGetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
