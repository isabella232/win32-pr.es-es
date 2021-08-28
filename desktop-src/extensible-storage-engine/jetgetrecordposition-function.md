---
description: 'Más información sobre: JetGetRecordPosition (Función)'
title: Función JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd1e84b995485afd46119b78289c1cac23e19215
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982438"
---
# <a name="jetgetrecordposition-function"></a>Función JetGetRecordPosition


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetrecordposition-function"></a>Función JetGetRecordPosition

La **función JetGetRecordPosition** devuelve la posición fraccionera del registro actual en el índice actual en forma de [JET_RECPOS](./jet-recpos-structure.md) estructura. Esta estructura describe las posiciones fraccionales en términos de un número aproximado de entradas de índice antes del registro actual y un número total aproximado de entradas en el índice.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*precpos*

Descripción de la fracción que se va a usar para obtener la posición del registro actual en el índice actual.

*cbRecpos*

Tamaño de memoria asignado en *precpos*.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Esta operación no se puede completar porque la instancia de , asociada a la sesión, encontró un error irreales. Es necesario revocar el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows 2000:</strong>  El sistema operativo Windows 2000 no devolverá este error.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El tamaño de la memoria asignada en <em>precpos</em> no es suficiente.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está actualmente en un registro y no puede devolver una posición.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows 2000:</strong>  El sistema operativo Windows 2000 no devolverá este error.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el número aproximado de entradas de índice que preceden al registro actual en el índice se devuelve en precpos- \> centriesLT. Se devuelve 1 en precpos- \> centriesInRange. El número aproximado de entradas del índice se devuelve en precpos- \> centriesTotal.

En caso de error, no se realiza ningún cambio en la memoria asignada en *precpos*.

#### <a name="remarks"></a>Observaciones

Esta operación devuelve datos variables cuando las actualizaciones se producen continuamente en la tabla. Los cambios en los valores no siempre coincidirán con las expectativas en función del conocimiento de las actualizaciones, ya que los valores son aproximaciones basadas en las propiedades físicas del índice. El aislamiento transaccional no se aplica a las posiciones de **JetGetRecordPosition,** ya que los valores dependen de propiedades físicas del índice que no están aisladas de transacciones.

[JET_RECPOS](./jet-recpos-structure.md) debe usarse para describir un registro dentro de una tabla o para cambiar la posición de un registro cerca de un registro existente. En su lugar, se deben recuperar los marcadores de un registro existente y, a continuación, se deben usar para cambiar la posición del mismo registro.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
