---
description: 'Más información sobre: JetGetSecondaryIndexBookmark (Función)'
title: JetGetSecondaryIndexBookmark (Función)
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
ms.openlocfilehash: d0773842d7de7d576e9ccbcab2c62ec456912a89
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984828"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark (Función)

La **función JetGetSecondaryIndexBookmark** recupera un marcador especial para la entrada de índice secundario en la posición actual de un cursor. A continuación, este marcador se puede usar para cambiar la posición eficaz de ese cursor a la misma entrada de índice [mediante JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Esto es muy útil al cambiar la posición en un índice secundario que contiene claves duplicadas o que contiene varias entradas de índice para el mismo registro.

**Windows XP: JetGetSecondaryIndexBookmark** se introdujo en Windows XP.

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

*tableid*

Cursor que se va a usar para esta llamada.

*pvSecondaryKey*

Búfer de salida que recibe la clave secundaria.

*cbSecondaryKeyMax*

Tamaño máximo, en bytes, del búfer de salida de la clave secundaria.

*milisegundoSecondaryKeyActual*

Recibe el tamaño real en bytes de la clave secundaria.

Si este parámetro es NULL, no se devolverá el tamaño real de la clave secundaria.

Si el búfer de salida es demasiado pequeño, se devolverá el tamaño real de la clave secundaria. Esto significa que este número será mayor que el tamaño del búfer de salida.

*pvPrimaryBookmark*

Búfer de salida que recibe el marcador de clave principal.

*cbPrimaryBookmarkMax*

Tamaño máximo, en bytes, del búfer de salida para el marcador de clave principal.

*pwPrimaryKeyActual*

Recibe el tamaño real, en bytes, del marcador de clave principal.

Si este parámetro es NULL, no se devolverá el tamaño real del marcador de clave principal.

Si el búfer de salida es demasiado pequeño, se devolverá el tamaño real del marcador de clave principal. Esto significa que este número será mayor que el tamaño del búfer de salida.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La operación se completó correctamente, pero uno de los búferes de salida era demasiado pequeño para recibir los datos solicitados.</p><p>El búfer de salida se ha rellenado con la mayor parte del marcador que cabría. También se ha devuelto el tamaño real del marcador, si se solicita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>El cursor no está actualmente en un índice secundario.</p><p>No es significativo recuperar un marcador de índice secundario cuando el cursor no usa actualmente un índice secundario. <a href="gg269221(v=exchg.10).md">JetGetBookmark debe</a> usarse cuando el cursor no está en un índice secundario.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está situado en un registro.</p><p>Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca actualmente después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el marcador de índice secundario de la entrada de índice en la posición actual de un cursor se devolverá en los búferes de salida. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado de los búferes de salida y el tamaño real del marcador de índice secundario serán indefinidos a menos que JET_errBufferTooSmall se devuelva. En caso de que se devuelva JET_errBufferTooSmall, los búferes de salida contendrán la mayor parte del marcador de índice secundario que cabe en el espacio proporcionado y el tamaño real del marcador de índice secundario será preciso. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Por lo general, los marcadores se deben tratar como fragmentos opacos de datos. No se debe intentar aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades sobre todos los marcadores de ESENT:

  - Un marcador identifica de forma única un registro en una tabla determinada.

  - El marcador de un registro no cambiará durante la vigencia de ese registro.

  - El marcador de un registro es el mismo que la clave de ese registro en el índice principal sobre la tabla que contiene ese registro. Si no se define ningún índice principal en esa tabla, el motor de base de datos creará su propio marcador para el registro.

  - Los marcadores se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su ordenación relativa en el índice principal sobre la tabla de los registros de origen. Si no se define ningún índice principal sobre esa tabla, el orden relativo de los marcadores de esa tabla no es significativo.

  - No tiene sentido comparar los marcadores de registros de tablas diferentes entre sí.

  - Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, los marcadores pueden ser mayores. El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.

Las claves generalmente se deben tratar como fragmentos opacos de datos. No se debe intentar aprovechar la estructura interna de estos datos. Sin embargo, se pueden conocer las siguientes propiedades sobre todas las claves DE ESENT:

  - Las claves se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su ordenación relativa en el índice de origen sobre la tabla de las entradas del índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser mayores. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
