---
description: 'Más información acerca de: JetRetrieveKey (función)'
title: Función JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083333"
---
# <a name="jetretrievekey-function"></a>Función JetRetrieveKey


_**Se aplica a:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>Función JetRetrieveKey

La función **JetRetrieveKey** recupera la clave de la entrada de índice en la posición actual de un cursor. Estas claves se crean mediante llamadas a [JetMakeKey](./jetmakekey-function.md). La clave recuperada se puede usar para devolver eficazmente ese cursor a la misma entrada de índice mediante una llamada a [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvData*

Búfer de salida que recibirá la clave.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*pcbActual*

Recibe el tamaño real en bytes de la clave.

Si este parámetro es NULL, no se devolverá el tamaño real de la clave.

Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real de la clave. Esto significa que este número será mayor que el tamaño del búfer de salida.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Cuando se especifica, el motor devolverá la clave de búsqueda para el cursor. La clave de búsqueda se basa en una o varias llamadas anteriores a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con el fin de buscar esa clave con <a href="gg294103(v=exchg.10).md">JetSeek</a> o establecer un intervalo de índice mediante <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>No hay ninguna clave de búsqueda actual para el cursor. Esto ocurrirá para <strong>JetRetrieveKey</strong> si se especifica JET_bitRetrieveCopy y no se ha construido una clave de búsqueda para este cursor mediante una llamada anterior a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. La clave de búsqueda se eliminará mediante una llamada anterior a cualquier API de navegación en el cursor que no sea <a href="gg294117(v=exchg.10).md">JetMove</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p></td>
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
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir toda la clave. El búfer de salida se ha rellenado con la gran parte de la clave que cabría. También se ha devuelto el tamaño real de la clave, si se solicita.</p>
<p><strong>Nota:</strong>   Este error no se devolverá si se especifica JET_bitRetrieveCopy. Vea la sección Comentarios para obtener más información.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la clave de la entrada de índice en la posición actual de un cursor se devolverá en el búfer de salida. Si se devuelve JET_wrnBufferTruncated, el búfer de salida contendrá la mayor parte de la clave que quepa en el espacio proporcionado y el tamaño real de la clave será preciso. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado del búfer de salida y el tamaño real de la clave serán indefinidos. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Por lo general, las claves se deben tratar como fragmentos opacos de datos. No se realiza ningún intento de aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades de todas las claves de ESENT:

  - Las claves se pueden comparar entre sí mediante la función [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para establecer su orden relativo en el índice de origen en la tabla de las entradas de índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser más grandes. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

Además de las propiedades anteriores de las claves ESENT en general, es importante tener en cuenta que una clave de búsqueda es diferente de la clave para una entrada de índice. En concreto, una clave de búsqueda puede ser más larga que una clave normal. Esta longitud adicional se produce cuando se utiliza una opción de carácter comodín al construir la clave de búsqueda. Vea [JetMakeKey](./jetmakekey-function.md) para obtener más información.

Hay un error importante en esta API que está presente en todas las versiones. Si la clave de búsqueda se solicita mediante el uso de JET_bitRetrieveCopy y el búfer de salida es demasiado pequeño para recibir toda la clave, no se devolverá JET_wrnBufferTruncated. Se devolverá JET_errSuccess en su lugar. Es importante comprobar que el tamaño real de la clave tal y como se devuelve mediante *pcbActual* es menor o igual que el tamaño del búfer de salida. Si el tamaño real es mayor que el tamaño del búfer de salida, el llamador de **JetRetrieveKey** debe reaccionar como si se devolvieran JET_wrnBufferTruncated en su lugar.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
