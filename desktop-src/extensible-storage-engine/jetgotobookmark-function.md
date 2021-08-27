---
description: 'Más información sobre: JetGotoBookmark (Función)'
title: JetGotoBookmark (Función)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f71956816ca09e9522bcd0e0c7c93e044baf387
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476431"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark (Función)

La **función JetGotoBookmark** coloca un cursor en una entrada de índice para el registro asociado al marcador especificado. El marcador se puede usar con cualquier índice definido en una tabla. El marcador de un registro se puede recuperar mediante [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Búfer que contiene el marcador que se usará para colocar el cursor.

*cbBookmark*

Tamaño del marcador en el búfer.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>   Este valor devuelto se introdujo en Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>El marcador proporcionado no es válido. Esto puede haber ocurrido porque el tamaño del marcador es cero o el puntero de búfer del marcador es <strong>NULL.</strong></p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor está en un índice secundario y no se pudo encontrar ninguna entrada de índice para el registro asociado al marcador.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRecordDeleted</p> | <p>No se encontró el registro asociado al marcador.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>   Este valor devuelto se introdujo en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el cursor se colocará en una entrada de índice para el registro asociado al marcador especificado. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanecerá sin cambios. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Hay dos maneras de usar un marcador para colocar un cursor en un índice. La primera es usar el marcador para colocar en el registro directamente. Esto sucede cuando el índice actual del cursor es el índice principal. Esta técnica funciona porque un marcador DE ESENT es el mismo que la clave principal del registro asociado.

La segunda manera de usar un marcador es colocarlo en una entrada de un índice secundario que se corresponda con el registro asociado a ese marcador. Durante este proceso, el motor busca el registro real mediante el marcador en el índice principal. A continuación, usa los datos de registro y la definición del índice secundario para calcular una clave en el índice secundario que apunta al registro. A continuación, coloca el cursor en la entrada de índice de esa clave. Si el cursor se encuentra actualmente en un índice secundario sobre una o varias columnas de clave con varios valores, el cursor se colocará en la entrada de índice correspondiente al primer valor múltiple de cada una de esas columnas de clave.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
