---
description: 'Más información sobre: JetMove (Función)'
title: Función JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 020018ede6be6ff13d65667deee5c189d98e1e53
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474061"
---
# <a name="jetmove-function"></a>Función JetMove


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetmove-function"></a>Función JetMove

La **función JetMove** coloca un cursor al principio o al final de un índice y recorre las entradas de ese índice hacia delante o hacia atrás. También es posible mover el cursor hacia delante o hacia atrás en el índice actual mediante un número especificado de entradas de índice. Otro enfoque es limitar artificialmente las entradas de índice que se pueden enumerar mediante **JetMove** mediante la configuración de un intervalo de índice en el cursor [mediante JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*Cuervo*

Desplazamiento arbitrario que indica el movimiento deseado del cursor en el índice actual.

Además de los desplazamientos estándar, este parámetro también se puede establecer con una de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>Mueve el cursor a la primera entrada de índice del índice (si existe).</p><p><strong>Nota</strong>   El valor literal de -2147483648 se usa para denotar esta opción. No use este valor como un desplazamiento normal o un comportamiento no deseado.</p> | 
| <p>JET_MoveLast</p> | <p>Mueve el cursor a la última entrada de índice del índice (si existe).</p><p><strong>Nota</strong>   El valor literal de 2147483647 se usa para denotar esta opción. No use este valor como un desplazamiento normal o un comportamiento no deseado.</p> | 
| <p>JET_MoveNext</p> | <p>Mueve el cursor a la siguiente entrada de índice del índice (si existe). Este valor es exactamente igual a un desplazamiento normal de +1.</p> | 
| <p>JET_MovePrevious</p> | <p>Mueve el cursor a la entrada de índice anterior del índice (si existe).</p><p>Este valor es exactamente igual a un desplazamiento normal de -1 o 0 (cero).</p><p>El cursor permanece en la posición lógica actual y se probará la existencia de la entrada de índice que corresponde a esa posición lógica.</p> | 



*grbit*

Grupo de bits que especifican cero o más de las siguientes opciones.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Mueve el cursor hacia delante o hacia atrás según el número de entradas de índice necesarias para omitir el número solicitado de valores de clave de índice encontrados en el índice. Esto tiene el efecto de contraer entradas de índice con valores de clave duplicados en una única entrada de índice. Normalmente, un desplazamiento moverá el cursor por el número especificado de entradas de índice, independientemente de sus valores de clave.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente. Para <strong>JetMove</strong>, esto significa que se encontró una entrada de índice en la ubicación o desplazamiento solicitados en el índice actual.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está situado actualmente en una entrada de índice. Para <strong>JetMove</strong>, esto significa que no se encontró una entrada de índice en la ubicación solicitada ni en el desplazamiento del índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Actualmente, el cursor se coloca lógicamente en una entrada de índice que corresponde a un registro que se ha eliminado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el cursor se colocará en una entrada de índice que coincida con la ubicación o desplazamiento solicitados. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si un intervalo de índice está en vigor y se JET_MoveFirst o JET_MoveLast, ese intervalo de índice se cancelará. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanecerá sin cambios a menos que JET_errNoCurrentRecord se devuelva. En ese caso, el cursor se colocará donde habría estado la entrada de índice que coincide con la ubicación o el desplazamiento solicitados. El cursor se puede mover con respecto a esa posición, pero todavía no está en una entrada de índice válida. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si un intervalo de índice está en vigor y se JET_MoveFirst o JET_MoveLast, ese intervalo de índice se cancelará. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Un cursor se puede mover a dos posiciones especiales mediante **JetMove**, Before First y After Last. Si el cursor está en la primera entrada de índice de la tabla y se llama a **JetMove** con JET_MovePrevious, se producirá un error en la llamada con JET_errNoCurrentRecord y el cursor se colocará lógicamente antes de la primera entrada del índice. Esta posición lógica se mantiene incluso si se inserta otra entrada de índice antes de la primera entrada del índice. Se produce una situación análoga para After Last con respecto al final del índice. Before First y After Last son más útiles al configurar un intervalo de entradas de índice que se van a iterar mediante **JetMove**, mediante un modelo de iterador que espera moverse siempre al siguiente (o anterior) elemento antes de usar ese elemento.

El conjunto de entradas de índice que puede visitar **JetMove** se puede limitar mediante la configuración de un intervalo de índice en el cursor. Esto es útil para las aplicaciones que enumeran un conjunto de entradas de índice que coinciden con criterios simples que se pueden expresar a través de un par de claves de búsqueda creadas para ese índice. Para obtener más información, [vea JetSetIndexRange](./jetsetindexrange-function.md).

En las versiones anteriores a Windows Server 2003 SP1, hay un problema en **JetMove** que se produce en algunos casos específicos, que afecta al cumplimiento correcto de un intervalo de índice configurado por la [función JetSetIndexRange.](./jetsetindexrange-function.md) Si el cursor está actualmente antes de la primera entrada de índice y se establece un intervalo de índice con un límite superior menor que la primera entrada de índice, la siguiente llamada a **JetMove** irá erróneamente a esa entrada de índice en lugar de dar error con JET_errNoCurrentRecord, según lo previsto. Se producirá el mismo error para la situación análoga a partir del final del índice. Esta situación puede producirse en una aplicación que configura un intervalo de índice y navega por él mediante un iterador que espera iniciarse antes de la primera entrada de índice que es miembro del conjunto de entradas que se van a enumerar, en lugar de iniciarse en la primera entrada de índice de ese conjunto. Esta situación también se produce en el caso análogo a partir del final del índice. La solución alternativa es que la aplicación compruebe manualmente que la entrada de índice adquirida está dentro del intervalo de índice comparando la clave de la entrada de índice actual (recuperada mediante [JetRetrieveKey)](./jetretrievekey-function.md)con la clave que representa el final del intervalo de índice actual (recuperado [mediante JetRetrieveKey](./jetretrievekey-function.md) mediante JET_bitRetrieveCopy).

Es importante tener cuidado al pasar desplazamientos calculados **a JetMove.** Si el desplazamiento calculado es menor o igual que JET_MoveFirst, ese desplazamiento debe dividirse en varias partes, cada una de las cuales se pasa a **JetMove** por separado, pero dentro de una sola transacción para obtener el efecto deseado. Lo mismo se aplica a los desplazamientos mayores o iguales que JET_MoveNext. Es poco probable que una aplicación se someta a esto en el mundo real, pero es bueno tener una defensa contra este caso dada la semántica muy diferente de JET_MoveFirst y JET_MoveLast desde un desplazamiento normal.

Cuando se llama a **JetMove** con un desplazamiento muy grande, como cuando el parámetro cRow se establece en 1000, **JetMove** recorre las 1000 entradas de índice para alcanzar la posición final. Actualmente, la API ese no proporciona una manera eficaz de moverse directamente a una entrada de índice determinada mediante desplazamiento sin atravesar cada entrada de índice.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
