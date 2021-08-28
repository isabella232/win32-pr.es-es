---
description: 'Más información sobre: JetSeek (Función)'
title: JetSeek (Función)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fbc980a838742971d2ecc3dfeebf5efb6295ea3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985548"
---
# <a name="jetseek-function"></a>JetSeek (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetseek-function"></a>JetSeek (Función)

La **función JetSeek** coloca eficazmente un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. Una clave de búsqueda se debe haber construido previamente [mediante JetMakeKey.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada. *Grbit* debe ser distinto de cero y debe incluir uno o varios de los valores enumerados en la tabla siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCheckUniqueness</p> | <p>Se devolverá un código de error especial, JET_wrnUniqueKey, si se puede determinar de forma económica que hay exactamente una entrada de índice que coincida con la clave de búsqueda.</p><p>Esta opción se omite a menos JET_bitSeekEQ también se especifique .</p><p>Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p> | 
| <p>JET_bitSeekEQ</p> | <p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que coincida exactamente con la clave de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de ese índice. El inicio del índice no es el mismo que el extremo bajo del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó <a href="gg269329(v=exchg.10).md">mediante JetMakeKey</a> mediante una opción de carácter comodín.</p> | 
| <p>JET_bitSeekGE</p> | <p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de ese índice. El inicio del índice no es el mismo que el extremo bajo del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al final del índice.</p> | 
| <p>JET_bitSeekGT</p> | <p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor que una entrada de índice que coincida exactamente con los criterios de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de ese índice. El inicio del índice no es el mismo que el extremo bajo del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p> | 
| <p>JET_bitSeekLE</p> | <p>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p> | 
| <p>JET_bitSeekLT</p> | <p>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor que una entrada de índice que coincida exactamente con los criterios de búsqueda. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>No tiene sentido usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> mediante una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al final del índice.</p> | 
| <p>JET_bitSetIndexRange</p> | <p>Se configurará automáticamente un intervalo de índice para todas las claves que coincidan exactamente con la clave de búsqueda. El intervalo de índice resultante es idéntico al que, de lo contrario, se habría creado mediante una llamada a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con las opciones JET_bitRangeInclusive y JET_bitRangeUpperLimit. Consulte <a href="gg294112(v=exchg.10).md">JetSetIndexRange para</a> obtener más información.</p><p>Se trata de un método práctico para detectar todas las entradas de índice que coinciden con los mismos criterios de búsqueda.</p><p>Esta opción se omite a menos JET_bitSeekEQ también se especifique .</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función permite la devolución de cualquier [JET_ERRs](./jet-err.md) definidas en esta API. Para obtener más información sobre los errores de Jet, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p><p>Para <strong>JetSeek</strong>, esto significa que se encontró una entrada de índice que coincidía exactamente con los criterios de búsqueda.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errKeyNotMade</p> | <p>No hay ninguna clave de búsqueda actual para el cursor. <strong>JetSeek requiere</strong> que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda usados para buscar entradas de índice.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRecordNotFound</p> | <p>No se encontró ninguna entrada de índice que coincida con los criterios de búsqueda.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_wrnSeekNotEqual</p> | <p>Se encontró una entrada de índice que coincidía con los criterios de búsqueda. Sin embargo, esa entrada de índice no era una coincidencia exacta.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_wrnUniqueKey</p> | <p>Se encontró exactamente una entrada de índice que coincidía exactamente con los criterios de búsqueda. Este error solo se devolverá si JET_bitSeekCheckUniqueness se especificó y era barato determinar que la entrada de índice correspondiente era la única entrada de índice que coincide exactamente con los criterios de búsqueda.</p><p>Este error solo lo devolverá Windows Server 2003 y versiones posteriores.</p> | 



Si se ejecuta correctamente, el cursor se colocará en una entrada de índice que coincida con los criterios de búsqueda. Si se ha preparado un registro para la actualización, se cancelará esa actualización. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos. Cuando varias entradas de índice tienen el mismo valor, siempre se selecciona la entrada más cercana al inicio del índice.

Si se produce un error, la posición del cursor permanecerá sin cambios a menos que JET_errRecordNotFound se devuelva. En ese caso, el cursor se colocará donde habría sido la entrada de índice que coincidía con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. El cursor se puede mover con respecto a esa posición, pero todavía no está en una entrada de índice válida. Si se ha preparado un registro para la actualización, se cancelará esa actualización. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
