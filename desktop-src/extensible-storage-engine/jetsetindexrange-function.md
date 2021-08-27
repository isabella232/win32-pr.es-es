---
description: 'Más información sobre: JetSetIndexRange (Función)'
title: Función JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 918d1c7f70f4f02158473ad4b97a510058787a6b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477471"
---
# <a name="jetsetindexrange-function"></a>Función JetSetIndexRange


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetindexrange-function"></a>Función JetSetIndexRange

La función **JetSetIndexRange** limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer mediante [JetMove](./jetmove-function.md) a las que comienzan desde la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados. Una clave de búsqueda se debe haber construido previamente [mediante JetMakeKey.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableidSrc*

Cursor que se va a usar para esta llamada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>Esta presencia o ausencia de esta opción indica los criterios de límite del intervalo de índice. Cuando está presente, esta opción indica que el límite del intervalo de índice es inclusivo. Cuando está ausente, esta opción indica que el límite del intervalo de índice es exclusivo. Cuando el límite del intervalo de índice es inclusivo, todas las entradas de índice que coincidan exactamente con los criterios de búsqueda se incluyen en el intervalo.</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>Esta opción solicita que se quite el intervalo de índice en cuanto se haya establecido. Todos los demás aspectos de la operación permanecen sin cambios. Esto es útil para probar la existencia de entradas de índice que coincidan con los criterios de búsqueda.</p> | 
| <p>JET_bitRangeRemove</p> | <p>Esta opción solicita que se cancele un intervalo de índice existente en el cursor. Una vez cancelado el intervalo de índice, será posible ir más allá del final del intervalo de índice <a href="gg294117(v=exchg.10).md">mediante JetMove</a>. Si un intervalo de índice aún no está en vigor, <strong>JetSetIndexRange</strong> producirá un error JET_errInvalidOperation.</p><p>Cuando se especifica esta opción, se omiten todas las demás opciones.</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>Si se usa esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda de la entrada de índice más cercana al final del índice que coincidirá con el intervalo de índice. El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias avanzando en el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un desplazamiento positivo.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p><p>Si se omite esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda de la entrada de índice más cercana al inicio del índice que coincidirá con el intervalo de índice. El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias si se retrocede en el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un desplazamiento negativo.</p><p>No tiene sentido omitir esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de comodín diseñada para buscar entradas de índice más cercanas al final del índice.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p><p>Para <strong>JetSetIndexRange</strong>, esto significa que se canceló un intervalo de índice existente o que hay al menos una entrada de índice dentro del intervalo de índice.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidOperation</p> | <p><strong>JetSetIndexRange</strong> devolverá este error cuando JET_bitRangeRemove especificado y no haya ningún intervalo de índice en vigor.</p> | 
| <p>JET_errKeyNotMade</p> | <p>No hay ninguna clave de búsqueda actual para el cursor. <strong>JetSetIndexRange requiere</strong> que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda usados para buscar entradas de índice.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>No hay ningún índice actual para el cursor. Esto ocurrirá para <strong>JetSetIndexRange</strong> si el cursor está en el índice clúster de una tabla, no se ha definido un índice principal. No se admite el establecimiento de un intervalo de índice sobre este tipo de índice.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p><strong>JetSetIndexRange</strong> devolverá este error para indicar que no hay entradas de índice dentro del intervalo de índice.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si la operación se JET_bitRangeRemove, se cancela el intervalo de índice que está actualmente en vigor. Si JET_bitRangeRemove no se especifica y se JET_bitRangeInstantDuration, no hay ningún intervalo de índice en vigor. Si no se JET_bitRangeRemove ni JET_bitRangeInstantDuration, hay un nuevo intervalo de índice en vigor. Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer mediante [JetMove](./jetmove-function.md) a las que comienzan desde la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda. La posición del cursor permanecerá sin cambios. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, JET_errNoCurrentRecord no se devuelve, no hay ningún intervalo de índice en vigor. Si JET_errNoCurrentRecord se devuelve, hay un nuevo intervalo de índice en vigor. Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer mediante [JetMove](./jetmove-function.md) a las que comienzan desde la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda. La posición del cursor permanecerá sin cambios. Si JET_errNoCurrentRecord y se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Un intervalo de índice es volátil y se cancelará automáticamente si se realiza alguna navegación que no sea [JetMove](./jetmove-function.md) en el cursor.

Los intervalos de índice solo funcionan en una dirección. Si se establece un límite superior, solo se impedirá el movimiento hacia delante mediante [JetMove](./jetmove-function.md) con JET_MoveNext o un desplazamiento positivo una vez que se haya alcanzado el final del intervalo de índice. Todavía es posible dejar el intervalo de índice en este caso mediante [JetMove](./jetmove-function.md) con JET_MovePrevious o un desplazamiento negativo. Se produce una situación análoga para un límite inferior.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
