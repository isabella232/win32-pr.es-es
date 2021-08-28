---
description: 'Más información sobre: JetIndexRecordCount (Función)'
title: JetIndexRecordCount (Función)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4105dec0217c1fea2e00d92c9d217fcf2d7e40b4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480441"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount (Función)

La **función JetIndexRecordCount** cuenta el número de entradas del índice actual desde la posición actual hacia delante. La posición actual se incluye en el recuento. El recuento puede ser mayor que el número total de registros de la tabla si el índice actual está sobre una columna con varios valores y las instancias de la columna tienen varios valores. Si la tabla está vacía, se devolverá 0 para el recuento.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pcrec*

Puntero a un valor long sin signo para recibir el recuento.

*crecMax*

Número máximo de registros que se cuentan. Un *valor crecMax* de 0 indica que el recuento es ilimitado.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está actualmente en un registro y la tabla no está vacía.</p><p><strong>Windows XP, Windows Server 2003, Windows 2000 Server y Windows 2000 Professional:</strong>  Si el cursor se coloca en un índice vacío o un intervalo de índice, <strong>JetIndexRecordCount</strong> devuelve erróneamente JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia de asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el número exacto de entradas de índice, incluida la posición actual y hasta *crecMax* (si no es 0), se devuelve en el valor long sin signo al que apunta *pcrec*.

Si se produce un error en esta función, no se realiza ningún cambio en la memoria asignada en *los objetos precpos*.

#### <a name="remarks"></a>Comentarios

Si la tabla no está vacía, el cursor debe colocarse en el registro desde el que se va a comenzar el recuento. El recuento incluirá este registro y el recuento se reenviará hasta el límite especificado en *crecMax*. Si *crecMax es* 0, la operación continuará contando hasta el final del índice.

Los intervalos de índice se pueden usar para construir limitaciones de final de índice artificiales para el recuento. De esta manera, los subrangos de un índice se pueden contar exactamente. El cursor debe colocarse en la primera fila del intervalo. Se debe establecer el final de la clave de intervalo y, a continuación, se debe usar [JetSetIndexRange](./jetsetindexrange-function.md) para establecer el intervalo superior, ya sea de forma inclusiva o exclusiva. Por último, se debe llamar a **JetIndexRecordCount** para contar exactamente el intervalo.

**JetIndexRecordCount sigue** la semántica de las transacciones y devuelve un recuento que es preciso para esta sesión determinada en su estado transaccional actual.

**JetIndexRecordCount accede** a las páginas hoja de índice para contar exactamente las entradas. Por lo tanto, puede realizar una gran cantidad de E/S y puede ser lenta. La *limitación crecMax* debe usarse para evitar una carga excesiva. Si un intervalo es grande, es posible contar el intervalo de forma aproximada mediante [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows Server 2003, Windows 2000 Server y Windows 2000 Professional:**  Si el cursor se coloca en un índice vacío o un intervalo de índice, **JetIndexRecordCount** devuelve erróneamente JET_errNoCurrentRecord en lugar de devolver un recuento de registros de cero. La aplicación debe comprobar si el índice o el intervalo de índice están vacíos en este caso.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
