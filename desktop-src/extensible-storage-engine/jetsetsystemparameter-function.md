---
description: 'Más información acerca de: JetSetSystemParameter (función)'
title: JetSetSystemParameter función)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275560"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter función)

La función **JetSetSystemParameter** se usa para establecer los numerosos valores de configuración del motor de base de datos.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parámetros

*pinstance*

Especifica la instancia de que se va a usar para esta llamada.

**Windows 2000:**  En Windows 2000, este parámetro se omite y siempre debe ser **null**.

**Windows XP:**  En Windows XP y versiones posteriores, este parámetro está ligeramente sobrecargado. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md). En cualquier caso, todos los parámetros del sistema se leen desde esa instancia. Si el motor está funcionando en modo de varias instancias, este parámetro puede ser **null** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateIndex](./jetcreateindex-function.md). Cuando este parámetro es **null** , se lee la configuración global del parámetro del sistema (o el valor predeterminado). Cuando este parámetro es una instancia, se lee el valor del parámetro del sistema para esa instancia.

Aunque técnicamente es un parámetro de salida, esta API nunca modifica el contenido del búfer proporcionado.

*sesid*

Especifica la sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.

*paramid*

IDENTIFICADOR del parámetro del sistema que se va a establecer. Vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.

*lParam*

Proporciona el valor que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.

*szParam*

Proporciona el valor para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.

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
<td><p>La operación se ha completado correctamente.</p>
<p><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores, se puede devolver Success sin un cambio en el valor del parámetro System. Para obtener más información, vea el JET_paramEnableAdvanced parámetro System en el tema <a href="gg269346(v=exchg.10).md">meta Parameters</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>La instancia se ha inicializado mediante una llamada a <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado. Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando se realiza un intento de configurar un parámetro del sistema después de que un cambio en su valor no pueda afectar al estado del motor de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Los parámetros de índice de tupla especificados no son válidos. Este error puede ser devuelto por <strong>JetSetSystemParameter</strong> solo cuando se establece <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</p>
<p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando:</p>
<ul>
<li><p>El ID. de parámetro del sistema especificado no es válido o no es compatible.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo permitido para el parámetro.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de la representación de la ruta de acceso absoluta estaba fuera del intervalo permitido para ese parámetro.</p>
<p><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo válido para el parámetro.</p></li>
<li><p>Se intentó establecer JET_paramUnicodeIndexDefault con un puntero JET_UNICODEINDEX <strong>null</strong> <a href="gg294097(v=exchg.10).md"></a> , un LCID no válido o un conjunto no admitido de marcas de LCMapString.</p>
<p><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</p></li>
<li><p>No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</p></li>
<li><p>Se ha intentado establecer un parámetro del sistema después de llamar a <a href="gg294068(v=exchg.10).md">JetInit</a> , el motor de base de datos está en modo de instancia única y no se ha especificado una sesión.</p>
<p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li>
<li><p>El parámetro del sistema especificado solo es global y se ha intentado establecer un valor específico de la instancia para ese parámetro del sistema.</p>
<p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li>
<li><p>El parámetro del sistema especificado solo es por instancia y se intentó establecer el valor global para ese parámetro del sistema.</p>
<p><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>La ruta de acceso del sistema de archivos especificada no era válida. Este error puede ser devuelto por <strong>JetSetSystemParameter</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p>
<p>Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</p>
<p>Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p>
<p><strong>Windows Vista:</strong>  Este error solo lo devolverán Windows Vista y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la configuración del parámetro System se establecerá en el valor proporcionado.

En caso de error, la configuración del parámetro System no se modificará.

#### <a name="remarks"></a>Observaciones

**JetSetSystemParameter** realiza un trabajo pobre al validar el valor elegido para cada parámetro del sistema. Se debe tener cuidado de no confiar en esta validación para aplicar una configuración correcta. Preste mucha atención a la descripción de cada parámetro del sistema y siga estas instrucciones para obtener una buena configuración de parámetros del sistema.

Hay un conjunto de parámetros del sistema que siempre se debe establecer para garantizar que el motor de base de datos funciona según lo previsto. En concreto, siempre debe establecerse cualquier parámetro del sistema que afecte al diseño físico de los archivos utilizados por el motor de base de datos. Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).

Cada parámetro del sistema tiene un valor predeterminado. Estos valores predeterminados han evolucionado a lo largo del tiempo y son bastante arbitrarios. Se recomienda encarecidamente que una aplicación evalúe todos los valores predeterminados para asegurarse de que son adecuados. Si no son adecuados, la aplicación debe configurarlos. Esto es importante, ya que muchos de estos parámetros pueden afectar en gran medida a la confiabilidad, el rendimiento y el uso de recursos del motor de base de datos.

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
<td><p>Se implementa como <strong>JetSetSystemParameterW</strong> (Unicode) y <strong>JetSetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
