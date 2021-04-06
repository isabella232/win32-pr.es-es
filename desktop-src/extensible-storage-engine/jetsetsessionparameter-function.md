---
description: 'Más información acerca de: JetSetSessionParameter (función)'
title: JetSetSessionParameter función)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001007"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter función)


_**Se aplica a:** Windows | Windows Server_

La función **JetSetSessionParameter** configura el motor de base de datos.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Especifica la sesión que se va a usar para esta llamada.

Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.

*sesparamid*

IDENTIFICADOR del parámetro de sesión que se va a establecer.

*pvParam*

Los datos que se van a establecer en este parámetro de sesión.

*cbParam*

Tamaño de los datos proporcionados.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente. Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>La instancia se ha inicializado mediante una llamada a la función <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado. Esto puede ocurrir cuando se intenta configurar un parámetro del sistema después de que un cambio en el valor del parámetro ya no afecte al estado del motor de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Los parámetros de índice de tupla especificados no son válidos. Este error solo se devuelve cuando el parámetro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> está establecido en un valor no válido. Para obtener información sobre estos parámetros, vea <a href="gg294119(v=exchg.10).md">parámetros de índice</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir cuando se produce lo siguiente:</p>
<ul>
<li><p>El ID. de parámetro del sistema especificado no es válido o no es compatible.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo permitido para el parámetro.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de la representación de la ruta de acceso absoluta estaba fuera del intervalo permitido para ese parámetro.</p></li>
<li><p>Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo válido para el parámetro.</p></li>
<li><p>Se intentó establecer JET_paramUnicodeIndexDefault con un puntero <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID no válido o un conjunto no admitido de marcas de <strong>LCMapString</strong> .</p></li>
<li><p>No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</p></li>
<li><p>Se ha intentado establecer un parámetro del sistema después de llamar a la función <a href="gg294068(v=exchg.10).md">JetInit</a> , el motor de base de datos está en modo de instancia única y no se ha especificado una sesión.</p></li>
<li><p>El parámetro del sistema especificado solo es global y se ha intentado establecer un valor específico de la instancia para ese parámetro del sistema.</p></li>
<li><p>El parámetro del sistema especificado solo es por instancia y se intentó establecer el valor global para ese parámetro del sistema.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>La ruta de acceso del sistema de archivos especificada no era válida. Este error puede ser devuelto por <strong>JetSetSessionParameter</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos. Por ejemplo, el parámetro <em>JET_paramSystemPath</em> puede devolver este error. Para obtener información acerca de este parámetro, consulte <a href="gg269235(v=exchg.10).md">parámetros del registro de transacciones</a>.</p></td>
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
<p>Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el parámetro del sistema se establecerá en el valor proporcionado.

En caso de error, el valor del parámetro del sistema permanecerá sin cambios.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Vea también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
