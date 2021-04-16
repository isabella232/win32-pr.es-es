---
description: 'Más información acerca de: JetSetLS (función)'
title: Función JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540766"
---
# <a name="jetsetls-function"></a>Función JetSetLS


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetls-function"></a>Función JetSetLS

La función **JetSetLS** permite a la aplicación asociar un identificador de contexto conocido como almacenamiento local con un cursor o la tabla asociada a ese cursor. La aplicación puede usar este identificador de contexto para almacenar datos auxiliares que están asociados a un cursor o una tabla. Posteriormente, la aplicación recibe una notificación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto. Esto hace posible asociar el estado asignado dinámicamente a un cursor o una tabla.

**Windows XP:**  **JetSetLS** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*ls*

Identificador de contexto que se va a asociar al cursor o a la tabla.

Cuando se especifica JET_bitLSReset, se omite el valor real de este parámetro y se usa JET_LSNil.

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
<td><p>JET_bitLSCursor</p></td>
<td><p>Esta opción indica que el identificador de contexto debe estar asociado al cursor especificado.</p>
<p>Si no se especifica ni JET_bitLSCursor ni JET_bitLSTable, se supone JET_bitLSCursor.</p>
<p>No se puede usar esta opción con JET_bitLSTable. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>Esta opción indica que se debe omitir el identificador de contexto especificado y que el identificador de contexto para el objeto elegido se debe restablecer en JET_LSNil.</p>
<p>Es importante tener en cuenta que esta acción no producirá una devolución de llamada para limpiar el valor anterior del identificador de contexto para el objeto elegido. La limpieza correcta del identificador de contexto anterior se puede lograr mediante <a href="gg269234(v=exchg.10).md">JetGetLS</a> con JET_bitLSReset. Vea <a href="gg269234(v=exchg.10).md">JetGetLS</a> para obtener más información.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Esta opción indica que el identificador de contexto se debe asociar a la tabla asociada al cursor especificado.</p>
<p>No se puede usar esta opción con JET_bitLSCursor. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p></td>
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
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usó de forma incorrecta o no se implementó. Esto puede ocurrir para <strong>JetSetLS</strong> cuando se especifican JET_bitLSCursor y JET_bitLSTable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>No se pudo asociar el identificador de contexto dado al objeto solicitado porque ya tenía un identificador de contexto asociado a él.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>No se pudo asociar el identificador de contexto dado al objeto solicitado porque la devolución de llamada en tiempo de ejecución no se ha configurado para la instancia asociada a la sesión.</p></td>
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
</tbody>
</table>


En caso de éxito, el identificador de contexto especificado se asoció correctamente al objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

El almacenamiento local de un cursor o una tabla debe verse como una caché volátil. En primer lugar, la aplicación debe intentar recuperar el identificador de contexto mediante [JetGetLS](./jetgetls-function.md). Si no se establece el valor (es decir, es JET_LSNil), la aplicación debe crear un nuevo contexto y cargarlo en la memoria caché mediante **JetSetLS**. La aplicación puede purgar la memoria caché mediante una llamada a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Si el motor de base de datos purga la memoria caché, se generará una devolución de llamada en tiempo de ejecución para dar a la aplicación la oportunidad de limpiar ese contexto. El tipo de devolución de llamada se JET_cbtypFreeCursorLS para un identificador de contexto asociado a un cursor y JET_cbtypFreeTableLS para un identificador de contexto asociado a una tabla. En cualquier caso, el identificador de contexto se pasará como pvArg1. Consulte [JET_CALLBACK](./jet-callback-callback-function.md) para obtener más información.

La devolución de llamada en tiempo de ejecución debe estar configurada correctamente para la instancia asociada a la sesión determinada antes de poder usar el almacenamiento local. Esta devolución de llamada se puede establecer mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramRuntimeCallback](./callback-parameters.md). Consulte [JetSetSystemParameter](./jetsetsystemparameter-function.md) y [JET_paramRuntimeCallback](./callback-parameters.md) en parámetros del sistema para obtener más información.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
