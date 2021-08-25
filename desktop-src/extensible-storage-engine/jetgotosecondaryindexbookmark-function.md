---
description: 'Más información sobre: JetGotoSecondaryIndexBookmark (Función)'
title: JetGotoSecondaryIndexBookmark (Función)
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
ms.openlocfilehash: ca8b05c0eeac88521d03b95a94f7d2363d5746e9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468952"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark (Función)

La **función JetGotoSecondaryIndexBookmark** coloca un cursor en una entrada de índice asociada al marcador de índice secundario especificado. El marcador de índice secundario debe usarse con el mismo índice en la misma tabla de la que se recuperó originalmente. El marcador de índice secundario de una entrada de índice se puede recuperar mediante **JetGotoSecondaryIndexBookmark**.

**Windows XP:****JetGotoSecondaryIndexBookmark** se introdujo en Windows XP.  

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

*tableid*

Cursor que se va a usar para esta llamada.

*pvSecondaryKey*

Búfer que contiene la clave secundaria que se usará para colocar el cursor.

*cbSecondaryKey*

Tamaño de la clave secundaria en el búfer.

*pvPrimaryBookmark*

Búfer que contiene el marcador de clave principal que se usará para colocar el cursor.

*cbPrimaryBookmark*

Tamaño del marcador de clave principal en el búfer.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>En caso de que ya no se pueda encontrar la entrada de índice, el cursor se colocará en la posición donde se encontró anteriormente esa entrada de índice. La operación seguirá con errores con JET_errRecordDeleted; sin embargo, será posible pasar a la entrada de índice siguiente o anterior en relación con la entrada de índice que ahora falta.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>El marcador de índice secundario que se proporcionó no era válido. Este error puede haber ocurrido porque la clave secundaria es cero o el puntero de búfer de clave secundario es <strong>NULL.</strong> Este error se produce porque</p><ul><li><p>El índice secundario actual no tiene una restricción de unidad y el tamaño del marcador proporcionado es cero.</p></li><li><p>El puntero de búfer de marcador es <strong>NULL.</strong></p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>El cursor no está actualmente en un índice secundario. No tiene sentido ir a un marcador de índice secundario cuando el cursor no usa actualmente un índice secundario. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> debe usarse cuando el cursor no está en un índice secundario.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRecordDeleted</p> | <p>No se encontró la entrada de índice asociada al marcador de índice secundario.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia de asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el cursor se colocará en una entrada de índice asociada al marcador de índice secundario especificado. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para que la use el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanece sin cambios, a menos que JET_errRecordDeleted se devuelva y JET_bitBookmarkPermitVirtualCurrency se especifique. En ese caso, el cursor se colocará donde habría sido la entrada de índice asociada al marcador de índice secundario especificado. El cursor se puede mover con respecto a esa posición, pero sigue sin estar en una entrada de índice válida.

Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para que la use el cursor, se eliminará esa clave de búsqueda. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
