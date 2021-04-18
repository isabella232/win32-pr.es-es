---
description: 'Más información acerca de: JetGetLS (función)'
title: JetGetLS función)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716963"
---
# <a name="jetgetls-function"></a>JetGetLS función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetls-function"></a>JetGetLS función)

La función **JetGetLS** permite que la aplicación recupere el identificador de contexto conocido como almacenamiento local que está asociado a un cursor o la tabla asociada a ese cursor. Este identificador de contexto se debe haber establecido previamente mediante [JetSetLS](./jetsetls-function.md). **JetGetLS** también se puede usar para capturar simultáneamente el identificador de contexto actual para un cursor o una tabla y restablecer ese identificador de contexto.

**Windows XP: JetGetLS** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pls*

Búfer de salida que recibe el identificador de contexto asociado actualmente al cursor o a la tabla.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

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
<td><p>Indica que se debe recuperar el identificador de contexto asociado al cursor especificado.</p>
<p>Si no se especifica ni JET_bitLSCursor ni JET_bitLSTable, se supone JET_bitLSCursor.</p>
<p>Esta opción no se puede utilizar con JET_bitLSTable. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indica que se debe recuperar el identificador de contexto asociado a la tabla que contiene el cursor especificado. No se puede usar esta opción con JET_bitLSCursor. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indica que el identificador de contexto para el objeto elegido debe restablecerse a JET_LSNil. El valor actual del identificador de contexto se devuelve en el búfer de salida.</p></td>
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
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usó de forma ilegal o no se implementó.</p>
<p>Esto puede ocurrir para <strong>JetGetLS</strong> cuando se establecen tanto JET_bitLSCursor como JET_bitLSTable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>No se pudo devolver el identificador de contexto porque actualmente no hay ningún identificador de contexto asociado al objeto solicitado.</p>
<p><strong>Nota:  </strong> Este error no se devuelve si se especifica JET_bitLSReset pero no se ha asociado ningún identificador de contexto al objeto solicitado.</p></td>
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
</tbody>
</table>


En caso de éxito, el identificador de contexto se recuperó correctamente del objeto solicitado. Si se especificó JET_bitLSReset, ese identificador de contexto también se quitó correctamente del objeto. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
