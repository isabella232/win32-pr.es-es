---
description: 'Más información acerca de: JetGotoSecondaryIndexBookmark (función)'
title: JetGotoSecondaryIndexBookmark función)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002113"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark función)

La función **JetGotoSecondaryIndexBookmark** coloca un cursor en una entrada de índice que está asociada al marcador de índice secundario especificado. El marcador de índice secundario debe usarse con el mismo índice en la misma tabla desde la que se recuperó originalmente. El marcador de índice secundario de una entrada de índice se puede recuperar mediante **JetGotoSecondaryIndexBookmark**.

**Windows XP:**  **JetGotoSecondaryIndexBookmark** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvSecondaryKey*

Búfer que contiene la clave secundaria que se va a usar para colocar el cursor.

*cbSecondaryKey*

Tamaño de la clave secundaria en el búfer.

*pvPrimaryBookmark*

Búfer que contiene el marcador de la clave principal que se va a usar para colocar el cursor.

*cbPrimaryBookmark*

Tamaño del marcador de la clave principal en el búfer.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>En caso de que ya no se pueda encontrar la entrada de índice, el cursor se dejará situado donde esa entrada de índice se haya encontrado previamente. La operación todavía producirá un error con JET_errRecordDeleted; sin embargo, será posible moverse a la entrada de índice siguiente o anterior en relación con la entrada de índice que ahora falta.</p></td>
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
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>El marcador de índice secundario proporcionado no era válido. Este error puede deberse a que la clave secundaria es cero o el puntero del búfer de clave secundaria es <strong>null</strong>. Este error se produce porque</p>
<ul>
<li><p>El índice secundario actual no tiene una restricción de unicidad y el tamaño del marcador proporcionado es cero.</p></li>
<li><p>El puntero de búfer de marcador es <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>El cursor no está actualmente en un índice secundario. No es significativo ir a un marcador de índice secundario cuando el cursor no está utilizando actualmente un índice secundario. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> debe usarse cuando el cursor no está en un índice secundario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>No se encontró la entrada de índice asociada al marcador de índice secundario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice asociada al marcador de índice secundario especificado. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha creado una clave de búsqueda para el cursor que se va a usar, se eliminará la clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanece inalterada a menos que se devuelva JET_errRecordDeleted y se especifique JET_bitBookmarkPermitVirtualCurrency. En ese caso, el cursor se colocará donde habría sido la entrada de índice asociada al marcador de índice secundario especificado. El cursor se puede mover con respecto a esa posición, pero todavía no está en una entrada de índice válida.

Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha creado una clave de búsqueda para el cursor que se va a usar, se eliminará la clave de búsqueda. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
