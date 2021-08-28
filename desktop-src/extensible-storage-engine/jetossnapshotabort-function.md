---
description: 'Más información sobre: JetOSSnapshotAbort (Función)'
title: JetOSSnapshotAbort (Función)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08e56bc95798559453c383549570f9470b55fa82
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474421"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort (Función)

La **función JetOSSnapshotAbort** notifica al motor que puede reanudar las operaciones de E/S normales una vez finalizado un período de inmovilización con una instantánea con error.

**Windows Server 2003:****JetOSSnapshotAbort** se introdujo en Windows Server 2003.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Opciones para esta llamada. Este parámetro está reservado para uso futuro y el único valor válido admitido es 0 (cero).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La sesión de instantánea no es válida o el parámetro grbit no es válido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 



Si esta función se realiza correctamente, la sesión de instantáneas finalizará y se reanudará el comportamiento normal del motor. Una nueva sesión de instantánea se puede iniciar en un momento posterior.

Si se produce un error en esta función, la sesión de instantánea no se anulará.

#### <a name="remarks"></a>Comentarios

Se debe llamar a esta función en lugar de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para informar al motor de que la instantánea se anuló por motivos que no están relacionados con el motor. Esta información se puede usar más adelante para ayudar a emitir mensajes del registro de eventos sobre la sesión de instantáneas o para ayudar a determinar otras acciones adecuadas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
