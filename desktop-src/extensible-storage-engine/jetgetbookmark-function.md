---
description: 'Más información sobre: JetGetBookmark (Función)'
title: JetGetBookmark (Función)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7806770d528d83f18d6f3eb061dc3043e15a0e53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984848"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetbookmark-function"></a>JetGetBookmark (Función)

La **función JetGetBookmark** recupera el marcador del registro asociado a la entrada de índice en la posición actual de un cursor. A continuación, este marcador se puede usar para volver a colocar ese cursor en el mismo registro [mediante JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Búfer de salida que recibe el marcador.

*cbMax*

Tamaño máximo, en bytes, del búfer de salida.

*actual*

Tamaño real, en bytes, del marcador.

Si este parámetro es **NULL,** no se devolverá el tamaño real del marcador.

Si el búfer de salida es demasiado pequeño, se devolverá el tamaño real del marcador. Esto significa que este número será mayor que el tamaño del búfer de salida.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el marcador completo. El búfer de salida se ha rellenado con la mayor parte del marcador que cabría. También se ha devuelto el tamaño real del marcador, si se solicita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong> Estos valores devueltos se introducen en Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no se coloca en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el marcador del registro asociado a la entrada de índice en la posición actual de un cursor se devolverá en el búfer de salida. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, el estado del búfer de salida y el tamaño real del marcador serán indefinidos a menos que JET_errBufferTooSmall se devuelva. En caso de JET_errBufferTooSmall, el búfer de salida contendrá la mayor parte del marcador que cabe en el espacio proporcionado y el tamaño real del marcador será preciso. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Normalmente, los marcadores se deben tratar como fragmentos opacos de datos. No se debe intentar aprovechar la estructura interna de estos datos. Sin embargo, se cumplen las condiciones siguientes en todos los marcadores DE ESENT:

  - Un marcador identifica de forma única un registro de una tabla determinada.

  - El marcador de un registro no cambiará durante la vigencia de ese registro.

  - El marcador de un registro es el mismo que la clave de ese registro en el índice principal sobre la tabla que contiene ese registro. Si no se define ningún índice principal sobre esa tabla, el motor de base de datos creará su propio marcador para el registro.

  - Los marcadores se pueden comparar entre sí mediante la función [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su ordenación relativa en el índice principal sobre la tabla de los registros de origen. Si no se define ningún índice principal sobre esa tabla, no es significativo usar la ordenación relativa de los marcadores de esa tabla.

  - No tiene sentido comparar marcadores de registros de tablas diferentes entre sí.

  - Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud, antes de Windows Vista.
    
**Windows Vista:** En Windows Vista y versiones posteriores, los marcadores pueden ser mayores JET_cbBookmarkMost (256) bytes. El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
