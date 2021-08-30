---
description: 'Más información sobre: JetGotoPosition (Función)'
title: JetGotoPosition (Función)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d36ef0b464eff95330aad482d4b6cdcf18668b6
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984618"
---
# <a name="jetgotoposition-function"></a>JetGotoPosition (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgotoposition-function"></a>JetGotoPosition (Función)

La **función JetGotoPosition** mueve un cursor a una nueva ubicación que es una fracción del camino a través del índice actual. La fracción es aproximadamente igual a la siguiente:

precpos- \> centriesLT/precpos- \> centriesTotal

Esta operación se realiza en respuesta a la entrada del cuadro de desplazamiento del usuario que se recibe cuando el usuario intenta mostrar datos que comienzan parcialmente a través de un conjunto de datos.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*precpos*

Descripción de la fracción que se usará para colocar el cursor en el índice actual.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se pudo completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se pudo completar porque la instancia de asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El valor precpos- cbStruct especificado no es un tamaño válido para la estructura &gt; <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> o precpos- centriesLT es mayor que &gt; precpos- &gt; centriesTotal.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Este error se devolverá si el índice está vacío.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el cursor se mueve a un registro actual que es una fracción del camino a través del índice donde la fracción es precpos- centriesLT dividida por \> precpos- \> centriesTotal.

Si se produce un error en esta función, la ubicación del cursor se deja sin modificar.

#### <a name="remarks"></a>Observaciones

Esta operación mueve el cursor a través de la tabla a una posición en el siguiente punto aproximado: precpos- \> centriesLT dividido por precpos- \> centriesTotal.

Cuando las actualizaciones se producen continuamente en la tabla, las llamadas posteriores con el mismo JET_RECPOS pueden mover el cursor [a](./jet-recpos-structure.md) distintas posiciones del índice, tanto antes como después de la posición anterior. El aislamiento transaccional no se [](./jet-recpos-structure.md) aplica al posicionamiento a través de JET_RECPOS, ya que depende de las propiedades físicas del índice que no están aisladas de la transacción.

[JET_RECPOS](./jet-recpos-structure.md) debe usarse para describir un registro dentro de una tabla o para cambiar la posición de un registro cerca de un registro existente. En su lugar, los marcadores de un registro existente se deben recuperar después de un **JetGotoPosition** inicial y, a continuación, usarse para cambiar la posición del mismo registro.

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
