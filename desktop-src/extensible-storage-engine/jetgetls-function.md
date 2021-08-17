---
description: 'Más información sobre: JetGetLS (Función)'
title: JetGetLS (Función)
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
ms.openlocfilehash: 3a359bb2899a2dea604e236a7118c914e795bffba7ca675229e28ad3a7f25dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979065"
---
# <a name="jetgetls-function"></a>JetGetLS (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetls-function"></a>JetGetLS (Función)

La **función JetGetLS** permite a la aplicación recuperar el identificador de contexto conocido como Storage local asociado a un cursor o a la tabla asociada a ese cursor. Este identificador de contexto se debe haber establecido previamente mediante [JetSetLS.](./jetsetls-function.md) **JetGetLS también** se puede usar para capturar simultáneamente el identificador de contexto actual para un cursor o tabla y restablecer ese identificador de contexto.

**Windows XP: JetGetLS** se introdujo en Windows XP.

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

*tableid*

Cursor que se va a usar para esta llamada.

*pls*

Búfer de salida que recibe el identificador de contexto asociado actualmente al cursor o la tabla.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSCursor</p></td>
<td><p>Indica que se debe recuperar el identificador de contexto asociado al cursor especificado.</p>
<p>Si no JET_bitLSCursor ni JET_bitLSTable se especifica , JET_bitLSCursor se supone que JET_bitLSCursor.</p>
<p>Esta opción no se puede usar con JET_bitLSTable. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indica que se debe recuperar el identificador de contexto asociado a la tabla que contiene el cursor especificado. No es posible usar esta opción con JET_bitLSCursor. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indica que el identificador de contexto del objeto elegido debe restablecerse a JET_LSNil. El valor actual del identificador de contexto se devuelve en el búfer de salida.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usaba de forma no válida o no se implementaba.</p>
<p>Esto puede ocurrir para <strong>JetGetLS</strong> cuando se JET_bitLSCursor y JET_bitLSTable de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>No se pudo devolver el identificador de contexto porque no hay ningún identificador de contexto asociado actualmente al objeto solicitado.</p>
<p><strong>Nota  </strong> Este error no se devuelve si JET_bitLSReset se especifica pero no se ha asociado ningún identificador de contexto con el objeto solicitado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
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


Si se realiza correctamente, el identificador de contexto se recuperó correctamente del objeto solicitado. Si JET_bitLSReset especificado, ese identificador de contexto también se quitó correctamente del objeto . No se producirá ningún cambio en el estado de la base de datos.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
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
