---
description: 'Más información acerca de: JetGetSecondaryIndexBookmark (función)'
title: JetGetSecondaryIndexBookmark función)
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716163"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark función)

La función **JetGetSecondaryIndexBookmark** recupera un marcador especial para la entrada de índice secundario en la posición actual de un cursor. Este marcador se puede usar para volver a colocar eficazmente ese cursor en la misma entrada de índice mediante [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Esto es muy útil cuando se cambia la posición en un índice secundario que contiene claves duplicadas o que contiene varias entradas de índice para el mismo registro.

**Windows XP: JetGetSecondaryIndexBookmark** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvSecondaryKey*

Búfer de salida que recibe la clave secundaria.

*cbSecondaryKeyMax*

Tamaño máximo, en bytes, del búfer de salida de la clave secundaria.

*pcbSecondaryKeyActual*

Recibe el tamaño real en bytes de la clave secundaria.

Si este parámetro es NULL, no se devolverá el tamaño real de la clave secundaria.

Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real de la clave secundaria. Esto significa que este número será mayor que el tamaño del búfer de salida.

*pvPrimaryBookmark*

Búfer de salida que recibe el marcador de la clave principal.

*cbPrimaryBookmarkMax*

Tamaño máximo, en bytes, del búfer de salida para el marcador de la clave principal.

*pcbPrimaryKeyActual*

Recibe el tamaño real, en bytes, del marcador de la clave principal.

Si este parámetro es NULL, no se devolverá el tamaño real del marcador de clave principal.

Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real del marcador de clave principal. Esto significa que este número será mayor que el tamaño del búfer de salida.

*grbit*

Reservado para uso futuro.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La operación se completó correctamente, pero uno de los búferes de salida era demasiado pequeño para recibir los datos solicitados.</p>
<p>El búfer de salida se ha rellenado con tanta parte del marcador como quepa. También se ha devuelto el tamaño real del marcador, si se solicita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>El cursor no está actualmente en un índice secundario.</p>
<p>No es significativo recuperar un marcador de índice secundario cuando el cursor no está utilizando actualmente un índice secundario. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> debe usarse cuando el cursor no está en un índice secundario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro.</p>
<p>Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p></td>
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
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá el marcador de índice secundario para la entrada de índice en la posición actual de un cursor en los búferes de salida. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado de los búferes de salida y el tamaño real del marcador de índice secundario será undefined, a menos que se devuelva JET_errBufferTooSmall. En el caso de que se devuelva JET_errBufferTooSmall, los búferes de salida contendrán tanto del marcador de índice secundario como quepan en el espacio proporcionado y el tamaño real del marcador de índice secundario será preciso. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Por lo general, los marcadores se deben tratar como fragmentos opacos de datos. No se realiza ningún intento de aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades de todos los marcadores de ESENT:

  - Un marcador identifica de forma única un registro en una tabla determinada.

  - El marcador de un registro no cambiará durante el período de duración de dicho registro.

  - El marcador de un registro es igual que la clave de ese registro en el índice principal de la tabla que contiene ese registro. Si no se define ningún índice principal sobre esa tabla, el motor de base de datos creará su propio marcador para el registro.

  - Los marcadores se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice principal sobre la tabla de los registros de origen. Si no se define ningún índice principal sobre esa tabla, el orden relativo de los marcadores de esa tabla no es significativo.

  - No tiene sentido comparar los marcadores de los registros de diferentes tablas entre sí.

  - Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud anterior a Windows Vista. En Windows Vista y versiones posteriores, los marcadores pueden ser más grandes. El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.

Por lo general, las claves se deben tratar como fragmentos opacos de datos. No se realiza ningún intento de aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades de todas las claves de ESENT:

  - Las claves se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice de origen en la tabla de las entradas del índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser más grandes. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

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
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
