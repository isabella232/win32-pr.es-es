---
description: 'Más información sobre: JetGetRecordSize (Función)'
title: JetGetRecordSize (Función)
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f42defeefa4d01648d34b971cce994fbebf8f0e8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481301"
---
# <a name="jetgetrecordsize-function"></a>JetGetRecordSize (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetrecordsize-function"></a>JetGetRecordSize (Función)

La **función JetGetRecordSize** recupera información de tamaño de registro de la ubicación deseada.

**Windows Vista: JetGetRecordSize** se introdujo en Windows Vista.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Identifica el contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Identifica la tabla o el cursor que se usará para la llamada API. El cursor debe estar situado en un registro o tener preparada una actualización.

*precsize*

Puntero a un búfer de salida para la [JET_RECSIZE](./jet-recsize-structure.md) estructura.

*grbit*

Este es uno o varios de los valores siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Esto recupera el tamaño del registro que se encuentra en el búfer de copia preparado para la actualización. De lo contrario, <em>el tableid</em> o el cursor deben colocarse en un registro y se usará ese registro.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Cuando se especifica este <a href="gg294072(v=exchg.10).md"></a> bit, el JET_RECSIZE no se reduce a cero antes de rellenar el contenido, actuando eficazmente como una acumulación de las estadísticas de varios registros visitados o actualizados.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Esto hace que la API ignore valores long no intrínsecos. Por ejemplo, solo se usará el registro local de la página.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Una de las opciones solicitadas no era válida o no se implementó. La función <strong>JetGetRecordSize</strong> devolverá este error cuando se especifique <em>un grbit</em> no seguro.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No es posible usar la misma sesión desde más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Esto puede ocurrir si el cursor se ha posicionado incorrectamente.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Si el cursor no se ha situado en una transacción, esto puede ocurrir si otro subproceso elimina el registro de en esta sesión.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se puede devolver si <strong>se</strong>ha pasado un tamaño<em>previo</em> NULL.</p> | 



#### <a name="remarks"></a>Comentarios

El tamaño de la clave acumulada en el **campo cbOverhead** [de](./jet-recsize-structure.md)JET_RECSIZE , se ve afectado por JET_bitRecordSizeInCopyBuffer. Si se especifica este bit, el tamaño de clave acumulado en el **campo cbOverhead** es el tamaño de clave completo. Si no se usa este bit, el tamaño de clave acumulado no incluirá ningún tamaño guardado debido a la compresión del prefijo de clave.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
